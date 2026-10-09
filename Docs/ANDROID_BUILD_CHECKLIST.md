# Android build checklist

## Current state
- The repository has been initialized with a README.
- The ZIP archive is available in the ChatGPT working session, but this integration cannot transfer local binary files directly to GitHub. The ZIP has **not** been committed to this repository.
- No APK build has run.

## Required next step: upload the archive
On GitHub mobile/web:
1. Open https://github.com/Eh333an/DreamHouse-MVP
2. Choose **Add file → Upload files**.
3. Select `DreamHouse_MVP_UnityProject (1).zip` from your device.
4. Wait for the upload to finish, then press **Commit changes**.
5. Confirm the ZIP appears on the repository's main page.

## Project validation in Unity
The archive contains C# gameplay scripts and supporting docs for a procedural MVP. It includes a Unity Editor helper and project settings, but the archive's scene folder contains only a scene README rather than a checked-in `.unity` scene. The editor setup/build process therefore needs to be run and verified in a compatible Unity Editor before the project can be called build-ready.

1. Extract the archive.
2. Open the folder containing `Assets` and `ProjectSettings` in Unity Hub.
3. Install the Android Build Support module with SDK/NDK and OpenJDK.
4. Let Unity compile scripts; resolve any compiler errors.
5. Run the project's editor setup menu, then verify that it creates/opens a playable scene and that all referenced assets are present.
6. Set Android as the build platform and use a unique package ID such as `com.dreamhouse.mvp`.
7. Build an APK and test on a physical Android device.

## MVP acceptance checklist
- Main menu opens without errors.
- Both characters can be selected.
- Touch joystick and camera work on Android.
- Living room, bedroom, and wardrobe are reachable.
- Outfit switching and simple interactions work.
- Missions/stars and save/load work after restarting.
- Stable frame rate and no missing assets on the target phone.

Do not distribute an APK until the above checks pass.
