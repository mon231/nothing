# nothing

An Android app that does nothing. It only shows a splash screen with the app's logo, and stays there.

## Requirements

- Android 5.0 (API 21) or higher

## Permissions

None. `AndroidManifest.xml` declares no permissions at all.

## The app

- One activity (`MainActivity`) extending `android.app.Activity` directly — no AppCompat, no libraries.
- Java only, no Kotlin.
- Black background, vector logo (concentric rings + center dot), the word `nothing`, and a tagline. That's it.

## Project layout

```
nothing/
├── app/
│   ├── build.gradle
│   └── src/main/
│       ├── AndroidManifest.xml
│       ├── java/com/nothing/app/MainActivity.java
│       └── res/
│           ├── drawable/                     (logo, launcher icon)
│           ├── layout/activity_main.xml      (splash screen)
│           ├── mipmap-anydpi-v26/            (adaptive launcher icon, API 26+)
│           ├── mipmap-anydpi/                (launcher icon fallback, API 21-25)
│           └── values/                       (colors, strings, theme)
├── .github/workflows/release.yml             (CI)
├── build.gradle
├── settings.gradle
└── README.md
```

## Building locally

You need JDK 17 and the Android SDK (with platform `android-34` installed).

This repo doesn't ship the Gradle wrapper jar — generate it once, then build:

```sh
gradle wrapper
./gradlew assembleRelease   # APK at app/build/outputs/apk/release/app-release.apk
./gradlew bundleRelease     # AAB at app/build/outputs/bundle/release/app-release.aab
```

By default the release build falls back to the debug signing key so the APK installs out of the box. The AAB it produces is **not** acceptable to Google Play — for that you need a real signing key (see below).

## Signing for Google Play

Google Play rejects bundles signed with the Android debug key. Generate a release keystore once and reuse it for every upload.

### 1. Generate a keystore

```sh
keytool -genkeypair -v \
  -keystore release.keystore \
  -alias nothing \
  -keyalg RSA -keysize 2048 -validity 10000
```

Pick a store password and a key password — keep them somewhere safe (a password manager). Losing this keystore means you can never publish an update to the same Play listing.

### 2. Build a signed release locally

Point the build at your keystore via env vars:

```sh
export RELEASE_KEYSTORE_PATH=/absolute/path/to/release.keystore
export RELEASE_KEYSTORE_PASSWORD='…'
export RELEASE_KEY_ALIAS=nothing
export RELEASE_KEY_PASSWORD='…'

./gradlew bundleRelease
```

The signed AAB lands at `app/build/outputs/bundle/release/app-release.aab` — upload that to the Play Console.

## Building via GitHub Actions

`.github/workflows/release.yml` runs on:

- **Every GitHub Release** (`release: created`) — builds the APK + AAB and attaches both to the release as assets.
- **Manual dispatch** (`workflow_dispatch`) — builds the APK + AAB and exposes them as workflow artifacts only.

It uses `gradle/actions/setup-gradle` with Gradle 8.2 directly, so the wrapper jar isn't required in CI.

### CI signing setup (required for Play-ready AABs)

Set these repository **secrets** in GitHub → Settings → Secrets and variables → Actions:

| Secret                       | Value                                                                 |
| ---------------------------- | --------------------------------------------------------------------- |
| `RELEASE_KEYSTORE_BASE64`    | `base64 -w0 release.keystore` (or `base64 < release.keystore` on Mac) |
| `RELEASE_KEYSTORE_PASSWORD`  | store password                                                        |
| `RELEASE_KEY_ALIAS`          | key alias (e.g. `nothing`)                                            |
| `RELEASE_KEY_PASSWORD`       | key password                                                          |

If `RELEASE_KEYSTORE_BASE64` is missing, the workflow still runs but logs a warning and produces debug-signed artifacts (the APK is fine for direct install; the AAB is **not** Play-acceptable).

### Cutting a release

1. Tag and push: `git tag v1.0.0 && git push --tags`
2. Create a GitHub Release for that tag.
3. The workflow builds and attaches `app-release.apk` and `app-release.aab` to the release.
4. Download the AAB and upload it to Google Play Console.

## License

Public domain. Do nothing with it.
