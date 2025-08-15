Play Store assets (placeholders created automatically):

- app-release.aab: located at `android/app/build/outputs/bundle/release/app-release.aab`
- icon-512.png: placeholder 512x512 icon copied from `mipmap-xxxhdpi/ic_launcher.png` (recommended 512x512 PNG).
- feature-1024x500.png: feature graphic required by Play Console (not generated).

Recommended assets to add before publishing:
- 512x512 app icon PNG (high-res)
- 1024x500 feature graphic PNG
- Screenshots: at least 2-3 phone screenshots (1080x1920 recommended)
- Promotional video (optional)

How to produce a real release AAB (locally on your Mac/PC):
1. Generate a release keystore locally with keytool and update `keystore.properties` with real values.
2. Restore the real `keystore.properties` (remove the disabled comment lines) and ensure `release.keystore` is placed in the project root.
3. From `android` folder run:

```powershell
.\gradlew.bat bundleRelease
```

4. Upload the generated `app-release.aab` to Play Console.

Notes:
- The current AAB is debug-signed because a production keystore was not available in this environment.
- Replace placeholder assets with production artwork before publishing.
