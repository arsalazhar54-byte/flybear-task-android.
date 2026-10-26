# Flybear Task Android APK project

This project packages the supplied Flybear Task HTML as an Android app using Capacitor.

## Build an APK in GitHub Actions (no Android Studio required)

1. Create a new repository on GitHub, for example `flybear-task-android`.
2. Upload the contents of this ZIP to the repository root (including the `.github` folder).
3. Open the repository's **Actions** tab and select **Build Flybear Task APK**.
4. Click **Run workflow** (or push a commit to `main` to trigger a build).
5. When the run finishes successfully, open the workflow run and download the artifact named `flybear-task-debug-apk`.
6. Extract the artifact ZIP to get `app-debug.apk`, then transfer it to your Android phone and install it.
   Android may ask you to allow installation from that browser/file manager. Only install APKs you built and trust.

## Important notes

- This is a debug APK for testing/sideloading, not a Play Store release.
- The HTML was kept mostly intact. The optional service-worker registration was disabled because no `sw.js` file was supplied.
- The app uses browser localStorage for user/task data. Data is stored locally in the app's WebView and is not automatically synchronized across phones.
- The source references `claude.use(...)` for some AI, cloud database, and download integrations. Those integrations are not provided by this Android wrapper and may not work unless you configure compatible services.
- Some external resources (Google Fonts and jsPDF) require an internet connection.
- Before using this app for important operational records, test login, task creation, photo saving, reports, PDF export, and reminders on your device.
