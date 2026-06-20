# Runoff DSS - Android app (Capacitor)

The app interface is bundled in `www/` (loads locally, no GitHub page).
It calls the Hugging Face backend online only for computation.

## How the APK is built (no Android Studio needed)
Push this repo to GitHub. The workflow in `.github/workflows/build-apk.yml`
builds the APK in the cloud automatically.

1. Create a new GitHub repo and upload these files.
2. Go to the Actions tab, the build runs on push (or click Run workflow).
3. When it finishes, open the run, download the `runoff-dss-apk` artifact.
4. Inside is `app-debug.apk` - install it on the phone.

## To change the interface later
Edit `www/index.html`, push, download the new APK. Backend changes on
Hugging Face apply automatically with no rebuild.

## Notes
- The app needs internet only for the backend computation.
- Debug APK is fine for sharing/testing. For Play Store, a signed release
  build is needed (can be added later).
