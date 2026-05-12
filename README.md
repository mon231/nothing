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
│           ├── drawable/logo.xml          (vector logo, also used as launcher icon)
│           ├── layout/activity_main.xml   (splash screen layout)
│           └── values/                    (colors, strings, theme)
├── .github/workflows/release.yml          (CI)
├── build.gradle
├── settings.gradle
└── README.md
```

## Building locally

You need JDK 17 and the Android SDK (with platform `android-34` installed).

This repo doesn't ship the Gradle wrapper jar — generate it once, then build:

```sh
gradle wrapper
./gradlew assembleRelease
```

The APK lands at:

```
app/build/outputs/apk/release/app-release.apk
```

The release build is signed with the debug key (config in `app/build.gradle`) so the APK installs out of the box. If you want to ship a real release, swap in your own `signingConfig`.

## Building via GitHub Actions

`.github/workflows/release.yml` runs on:

- **Every GitHub Release** (`release: created`) — builds the APK and attaches it to the release as an asset.
- **Manual dispatch** (`workflow_dispatch`) — builds the APK and exposes it as a workflow artifact only.

It uses `gradle/actions/setup-gradle` with Gradle 8.2 directly, so the wrapper jar isn't required in CI.

To cut a release:

1. Tag and push: `git tag v1.0.0 && git push --tags`
2. Create a GitHub Release for that tag.
3. The workflow builds and attaches `app-release.apk` to the release.

## License

Public domain. Do nothing with it.
