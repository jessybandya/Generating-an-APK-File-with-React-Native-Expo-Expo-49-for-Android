# Generating an APK File with React Native Expo (Expo 49) for Android

This guide demonstrates the steps to create an APK file for Android using React Native Expo based on Expo version 49.

## Prerequisites

- Node.js installed on your system
- Expo CLI globally installed (`npm install -g expo-cli`)

## Steps

### Step 1: Install EAS CLI

Install the EAS CLI by running the following command in your terminal:

```bash
npm install -g eas-cli
```

### Step 2: Login to Expo Dashboard

If you're not logged in to the Expo dashboard, use the following command to log in:

```bash
eas login
```

### Step 3: Create `eas.json` Configuration

If you don't have an `eas.json` file in the root directory of your app, create one and add the following content:

```json
{
  "cli": {
    "version": ">= 5.9.1"
  },
  "build": {
    "development": {
      "developmentClient": true,
      "distribution": "internal"
    },
    "preview": {
      "distribution": "internal",
      "android": {
        "buildType": "apk"
      }
    },
    "production": {}
  },
  "submit": {
    "production": {}
  }
}
```

### Step 4: Build APK using EAS

Run the following command to build the APK file using EAS:

```bash
eas build --profile preview --platform android
```

This command will start the build process and generate the APK file for Android.

## Notes

- Make sure to replace `your-app-name` with your actual app name.
- Adjust configurations in `eas.json` as needed for different build types or settings.

---

Kindly make sure there's no collision of dependancies' versions especially navigation dependancies to avoid build failure.


 # HAPPY CODING
