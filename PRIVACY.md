# Privacy Policy for **nothing**

**Effective date:** 2026-05-12
**Last updated:** 2026-05-12

---

## Summary

**nothing** is an Android application that does nothing. It displays a splash screen with the application's logo and remains on that screen until the user closes it.

The application:

- Does **not** collect any personal information.
- Does **not** transmit any data over the network.
- Does **not** request any Android runtime or install-time permissions.
- Does **not** store any data on the device beyond what the Android operating system stores automatically for every installed application.
- Does **not** include any third-party libraries, advertising SDKs, analytics SDKs, or crash-reporting SDKs.
- Does **not** use cookies, web tracking technologies, or device identifiers.

If you install **nothing** and open it, the application performs no I/O of any kind beyond rendering its own user interface.

The remainder of this document expands on the above in the form expected by app store policies and applicable data protection laws.

---

## 1. Introduction

This Privacy Policy ("Policy") describes how the **nothing** Android application ("the App", "we", "us", or "our") handles information in connection with your use of the App. This Policy is provided to comply with the Google Play Developer Program Policies, the EU General Data Protection Regulation 2016/679 ("GDPR"), the UK General Data Protection Regulation ("UK GDPR"), the California Consumer Privacy Act of 2018 as amended by the California Privacy Rights Act ("CCPA/CPRA"), the U.S. Children's Online Privacy Protection Act ("COPPA"), and analogous data protection legislation in other jurisdictions.

By installing or using the App, you acknowledge that you have read and understood this Policy.

The App is offered free of charge, with no in-app purchases, no advertisements, no user accounts, and no server-side component.

## 2. Information We Do Not Collect

We want to be explicit about the categories of information that the App does **not** collect, because this enumeration is what Google Play, the GDPR, and the CCPA expect to be addressed regardless of whether collection actually occurs.

The App does not collect, process, store, or transmit any of the following:

- **Identity information**: name, username, email address, phone number, date of birth, government-issued identifiers, or any other information that could be used to identify you.
- **Account information**: the App has no concept of a user account. No sign-in, no registration, no profile.
- **Contact information**: your contacts, address book, call logs, or SMS messages.
- **Location data**: precise (GPS) or approximate (network-derived) location, IP-address-derived location, or any other geolocation signal.
- **Device identifiers**: Android Advertising ID (AAID), Android ID, IMEI, MAC address, serial number, hardware identifiers, or any other persistent identifier.
- **Network information**: IP address, network operator, Wi-Fi SSID, Bluetooth peer information, or connection state.
- **Device characteristics**: model, manufacturer, OS version, screen size, language, timezone, or installed-app inventory.
- **Usage data**: which screens you view, how long you keep the App open, taps, gestures, scroll depth, session length, or any other interaction telemetry.
- **Performance data**: crash reports, ANR reports, performance traces, memory usage, or battery usage attributable to the App.
- **Content**: photos, videos, documents, files, microphone audio, camera images, or any other media or content from your device.
- **Sensor data**: accelerometer, gyroscope, magnetometer, ambient light, proximity, fingerprint, face, or any other sensor reading.
- **Health and fitness data**: steps, heart rate, or any other health-related signal.
- **Financial information**: payment instruments, transactions, or balances. The App is free and contains no in-app purchases.
- **Authentication data**: passwords, tokens, biometric templates, or credentials of any kind.
- **Communications**: messages, emails, or any other content you produce.

The App also does not derive, infer, or generate any personal information from on-device computation.

## 3. Android Permissions

The App declares **zero** permissions in its `AndroidManifest.xml` file. It does not request any install-time permissions, runtime permissions, or special permissions (such as Accessibility Service, Device Administrator, Notification Listener, or "All files access").

You can verify this for yourself in your device settings:

- **Android 6.0+:** Settings → Apps → nothing → Permissions. The list will be empty.
- All Android versions: the Google Play listing's "Data safety" section discloses that no data is collected and no permissions are requested.

Because the App requests no permissions, it cannot access your camera, microphone, location, contacts, storage, network, or any other sensitive resource — even if it tried.

## 4. Data Storage on Your Device

The App does not write to any persistent storage. It does not create files, does not use SharedPreferences, does not open a database, and does not cache anything.

The only on-device storage associated with the App is the storage that the Android operating system maintains for every installed application: the APK file itself, a small private data directory (which the App leaves empty), and standard system metadata. This is managed by Android, not by the App, and is removed automatically when you uninstall the App.

## 5. Network and Internet Activity

The App makes **no** network connections. It does not contact any server operated by us or by any third party. It does not download configuration, content, ads, or updates at runtime. It does not phone home.

The App does not declare the `android.permission.INTERNET` permission, which means the Android operating system will block any attempted network access from the App's process.

## 6. Third-Party Services and SDKs

The App contains **no** third-party libraries, SDKs, or services. Specifically, it does not integrate any of the following:

- Advertising networks (e.g., Google AdMob, Meta Audience Network, Unity Ads).
- Analytics platforms (e.g., Google Analytics for Firebase, Mixpanel, Amplitude, Segment).
- Crash reporting (e.g., Firebase Crashlytics, Sentry, Bugsnag).
- Attribution / Mobile Measurement Partners (e.g., AppsFlyer, Adjust, Branch).
- Push notification services (e.g., Firebase Cloud Messaging, OneSignal).
- Authentication providers (e.g., Sign in with Google, Facebook Login).
- Social-network SDKs (e.g., Facebook SDK, Twitter Kit).
- Payment processors.
- Cloud storage SDKs.
- AndroidX, Jetpack, or AppCompat libraries.

The App is built only against the Android platform framework (no `dependencies {}` in `app/build.gradle`).

## 7. Analytics, Crash Reporting, and Telemetry

There is no analytics, crash reporting, or telemetry of any kind. We do not know when you install the App, when you open it, how often you open it, or whether it crashes on your device. The only aggregate information we may receive is what Google Play makes available to all developers in the Play Console (e.g., country-level install counts, crash counts derived by Android Vitals from the operating system itself). This information is generated by Google, governed by Google's privacy policy, and is not collected or processed by us beyond viewing the aggregated reports.

## 8. Advertising

The App contains no advertising. We do not use the Android Advertising ID. We do not participate in any ad network, real-time bidding system, or ad measurement program.

## 9. Children's Privacy

The App is suitable for users of all ages and is designed in compliance with the U.S. Children's Online Privacy Protection Act ("COPPA"), the EU GDPR (including Article 8 protections for children), and Google Play's Families Policy.

Because the App collects **no** information whatsoever, it does not knowingly collect any personal information from anyone, including children under the age of 13 (or under the equivalent minimum age in the relevant jurisdiction). There is no mechanism by which the App could collect such information, even inadvertently.

If a parent or legal guardian believes that, despite the App's design, their child has somehow had personal information collected, they may contact us using the details in Section 15. We will respond promptly, although we do not anticipate that any such information exists for us to investigate.

## 10. Your Rights Under Data Protection Laws

Although we do not collect or process any personal data, the data protection laws below grant you certain rights with respect to a controller's processing of your personal data. We summarize them here for completeness.

### 10.1. European Economic Area, United Kingdom, and Switzerland (GDPR / UK GDPR)

If you are located in the EEA, the UK, or Switzerland, you have the right to:

- **Access** any personal data we hold about you.
- **Rectify** inaccurate personal data.
- **Erase** ("right to be forgotten") personal data we hold about you.
- **Restrict** processing of your personal data.
- **Object** to processing.
- **Data portability** — receive your personal data in a structured, machine-readable format.
- **Withdraw consent** at any time, where processing is based on consent.
- **Lodge a complaint** with your local supervisory authority.

Because we do not collect or process any personal data, there is nothing to access, rectify, erase, restrict, port, or withdraw. Any access or erasure request we receive will be answered with confirmation that no data is held.

The legal basis for processing under GDPR Article 6 is not applicable, because no processing of personal data occurs.

### 10.2. California (CCPA / CPRA)

If you are a California resident, the CCPA / CPRA grants you the right to:

- Know what categories of personal information are collected, the sources, the purposes, and the categories of recipients.
- Access the specific pieces of personal information collected about you.
- Delete personal information collected from you.
- Correct inaccurate personal information.
- Opt out of the "sale" or "sharing" of personal information.
- Limit the use and disclosure of sensitive personal information.
- Non-discrimination for exercising any of these rights.

We disclose for completeness that, in the twelve months preceding the effective date of this Policy and at all times since:

- We have **not** collected any of the categories of personal information enumerated in Cal. Civ. Code § 1798.140(v).
- We have **not** sold or shared any personal information.
- We have **not** used or disclosed any sensitive personal information.

You may submit a verifiable consumer request using the contact details in Section 15. Such a request will be answered with confirmation that no personal information is held.

### 10.3. Other Jurisdictions

The App is designed to be compliant with analogous data protection regimes including, without limitation, Brazil's LGPD, Canada's PIPEDA, Australia's Privacy Act 1988, Japan's APPI, and South Korea's PIPA. Because no personal data is collected or processed, the substantive obligations of those regimes are not engaged.

## 11. International Data Transfers

Because no personal data is collected, no personal data is transferred — internationally or otherwise.

## 12. Data Retention

Because no personal data is collected, no personal data is retained. The App holds no records about you that could be retained, deleted, or anonymized.

## 13. Security

While we do not hold any user data that could be compromised, the App is built using the Android platform's standard security model: it runs in its own application sandbox, holds no permissions, opens no IPC endpoints, and does not expose any `Activity`, `Service`, `BroadcastReceiver`, or `ContentProvider` to other applications beyond the launcher activity required by Android to display the App in the launcher.

The release artifact (APK and AAB) is signed using standard Android cryptographic signing.

## 14. Changes to This Privacy Policy

We may update this Privacy Policy from time to time, for example to reflect changes in the law or to clarify our practices. When we do, we will update the "Last updated" date at the top of this document and publish the revised Policy at the same URL where you found this one. Material changes will be communicated through the application's listing on Google Play, where applicable.

Your continued use of the App after a revised Policy is published constitutes your acceptance of that revised Policy. If you do not agree to the revised Policy, you must uninstall the App.

## 15. Contact

If you have questions, comments, or requests regarding this Privacy Policy or your rights under applicable data protection laws, you may contact the developer at:

- **Email:** avarti765@gmail.com
- **Source code & issues:** https://github.com/mon231/nothing

We will endeavour to respond to verifiable requests within thirty (30) days, or sooner where required by applicable law.

---

*This Privacy Policy is licensed for any use, modification, or redistribution under the terms of the [Creative Commons CC0 1.0 Universal Public Domain Dedication](https://creativecommons.org/publicdomain/zero/1.0/). It is provided "as is" and does not constitute legal advice.*
