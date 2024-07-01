# Mobile Security Game Project


## Project Setup and Bug Fixes

### Creating the Android Project

1. **Create a New Android Project**
    - Open Android Studio and create a new Android project.

2. **Copy Necessary Files**
    - Decompiled the APK using an online decompiler.
    - Copied all necessary source files, resources, and other components from the decompiled APK into the new Android project.

### Bug Fixes

1. **Fixed Toast Message Duration**
    - Changed the duration value from `1` to `Toast.LENGTH_LONG` to display the messages correctly.

2. **Add INTERNET Permission to Manifest**
    - Added the following permission to `AndroidManifest.xml` to allow network operations:
      ```xml
      <uses-permission android:name="android.permission.INTERNET"/>
      ```

3. **Add URL to Strings and Fix It**
   - Added the URL to the `strings.xml` for better management


4. **Handled Short ID Issues**
    - Added checks to ensure the ID length is at least 8 characters before processing. This prevents crashes due to short IDs.

## How to Play the Game

The way to survive in the game is by clicking on the characters in the correct order. Each digit entered in the ID modulo 4 represents a direction:
- `0` - Left
- `1` - Right
- `2` - Up
- `3` - Down

Follow the sequence generated from your ID to "survive."

### Result of Toast Message

If you manage to "survive" by clicking the characters in the correct order, a toast message will display the name of the town you reached. For example, I arrived in Washington.
