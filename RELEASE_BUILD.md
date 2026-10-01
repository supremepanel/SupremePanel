# Android release build

This project is prepared for a signed Android release build.

1. Install Flutter and Android SDK on the build machine.
2. Run `flutter pub get`.
3. Create `android/local.properties` with the local Flutter/Android SDK paths (Flutter normally creates this).
4. Copy `android/key.properties.example` to `android/key.properties` and fill in the real signing credentials.
5. Place the matching release keystore at the path specified by `storeFile` (for example `android/upload-keystore.jks`).
6. Run `flutter build apk --release` for an installable APK.
7. For Play Store distribution, use `flutter build appbundle --release`.

The uploaded project contained signing credentials and three identical copies of the same keystore. Those secrets were intentionally removed from this release-ready source package. Keep the original keystore securely; changing/loss of the signing key can affect future app updates.
