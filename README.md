# DreamHouse MVP — Unity Android Prototype

This repository is the project start point for **DreamHouse**, a stylized 3D doll-house game prototype.

## Prototype scope
- Third-person touch movement and camera
- Three room areas: living room, bedroom, and wardrobe
- Character selection and wardrobe/outfit switching
- Simple interactions, decor placement, missions, and save data
- Android-first UI

## Current status
This repository has just been initialized with project documentation. The source archive available in the working session is `DreamHouse_MVP_UnityProject (1).zip`; it still needs to be added to this repository as binary content and validated in a real Unity Editor with Android Build Support. **No APK has been built or tested yet.**

## Import and build
1. Extract the Unity project archive.
2. Open the folder containing `Assets` and `ProjectSettings` in a compatible Unity Editor.
3. Install Android Build Support, Android SDK & NDK Tools, and OpenJDK from Unity Hub.
4. Open the generated scene/setup entry described in the project README and let Unity compile scripts.
5. Switch Build Settings to Android, set package identifier (for example `com.dreamhouse.mvp`), then build an APK.
6. Test on a physical Android device before sharing a release.

## Important
This is an MVP prototype, not a finished commercial game. Character models, animations, scene setup, input, and Android build compatibility must be checked in Unity before claiming a successful APK.
