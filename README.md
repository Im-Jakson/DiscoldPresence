# Discold Presence
**Your Games, Your Presence.**

Android Kotlin starter project (v0.1.0). Dark UI, installed-app selector, Usage Access permission flow, foreground-app check, and local session timer preview.

## Build
1. Open this folder in Android Studio (Giraffe or newer).
2. Let Gradle sync.
3. Build > Build Bundle(s) / APK(s) > Build APK(s).
4. Install the debug APK on an Android device.

## Current scope
This is a functional UI/prototype foundation, not a finished Discord Rich Presence client. Android can list launchable apps and, with the user's explicit Usage Access permission, inspect recent foreground-app events. It does not silently monitor or transmit activity.

## Discord integration boundary
Do not paste a personal Discord user token into this app. User-token automation/self-bots are not an approved integration. Bot tokens do not grant Rich Presence for a user's personal account. A legitimate Rich Presence implementation must use Discord's supported SDK/RPC integration and meet its platform and application requirements. The SDK path may require integration inside the game; it does not guarantee a separate Android companion app can publish arbitrary presence for any installed app.

The `DiscordPresenceAdapter` is intentionally not implemented until the supported Discord integration method and app eligibility are confirmed.

## Build APK online from a phone with GitHub Actions
1. Create a GitHub repository and upload the contents of this project (including the hidden `.github` folder).
2. Open the repository's **Actions** tab and select **Build Discold Presence APK**.
3. Tap **Run workflow** (or wait for the first push build).
4. Open the completed workflow run, find **Artifacts**, and download `Discold-Presence-debug`.
5. Extract the downloaded artifact ZIP to get `app-debug.apk`, then install it on Android.

This workflow compiles the starter only. Discord publishing is not implemented yet.
