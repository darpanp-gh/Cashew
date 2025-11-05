# Ledgerly - Installation & Setup Guide

## 📋 Prerequisites

Before building Ledgerly, ensure you have the following installed:

### Required Software
- **Flutter SDK** (3.0 or higher)
  - Download from: https://flutter.dev/docs/get-started/install
- **Dart SDK** (included with Flutter)
- **Git** (for version control)

### Platform-Specific Requirements

#### For Android Development:
- **Android Studio** (latest version recommended)
- **Android SDK** (API 23 or higher)
- **Java Development Kit (JDK)** 8 or higher

#### For iOS Development (macOS only):
- **Xcode** (latest version)
- **CocoaPods** (for iOS dependencies)
- **iOS SDK**

---

## 🚀 Quick Start

### Step 1: Verify Flutter Installation

```bash
flutter doctor
```

This command checks your environment and displays a report of the status of your Flutter installation. Resolve any issues before proceeding.

### Step 2: Navigate to Project Directory

```bash
cd /app/budget
```

### Step 3: Get Dependencies

```bash
flutter pub get
```

This downloads all the required packages listed in `pubspec.yaml`.

### Step 4: Run the App

**For Android/iOS Device or Emulator:**
```bash
flutter run
```

**For Web (if enabled):**
```bash
flutter run -d chrome
```

---

## 🏗️ Building Release Versions

### Android

#### Build APK (for testing/distribution):
```bash
flutter build apk --release
```
Output location: `/app/budget/build/app/outputs/flutter-apk/app-release.apk`

#### Build App Bundle (for Play Store):
```bash
flutter build appbundle --release
```
Output location: `/app/budget/build/app/outputs/bundle/release/app-release.aab`

### iOS (macOS only)

#### Build for iOS Device:
```bash
flutter build ios --release
```

#### Build IPA (for App Store/TestFlight):
```bash
flutter build ipa
```
Output location: `/app/budget/build/ios/ipa/`

---

## 🔧 Configuration

### App Signing (Android)

For release builds, you may need to configure signing. Create a file `android/key.properties`:

```properties
storePassword=<your-store-password>
keyPassword=<your-key-password>
keyAlias=<your-key-alias>
storeFile=<path-to-your-keystore>
```

**Note:** For academic purposes, signing may not be required.

### App Signing (iOS)

iOS builds require Apple Developer account and proper provisioning profiles. For academic purposes, you can run on simulator without signing.

---

## 📱 Running on Devices

### Android Device

1. Enable Developer Options on your Android device
2. Enable USB Debugging
3. Connect device via USB
4. Run: `flutter devices` to verify connection
5. Run: `flutter run`

### iOS Device (macOS only)

1. Connect your iOS device via USB
2. Trust the computer on your device
3. Open the project in Xcode if needed
4. Run: `flutter run`

### Emulators/Simulators

**Android Emulator:**
```bash
# List available emulators
flutter emulators

# Launch an emulator
flutter emulators --launch <emulator-id>

# Run app
flutter run
```

**iOS Simulator (macOS only):**
```bash
open -a Simulator
flutter run
```

---

## 🐛 Troubleshooting

### Common Issues

#### 1. "Flutter command not found"
**Solution:** Add Flutter to your PATH
```bash
export PATH="$PATH:`pwd`/flutter/bin"
```

#### 2. "Unable to locate Android SDK"
**Solution:** Set ANDROID_HOME environment variable
```bash
export ANDROID_HOME=$HOME/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/platform-tools
```

#### 3. Gradle build errors
**Solution:** 
- Clean the build: `flutter clean`
- Get dependencies: `flutter pub get`
- Rebuild: `flutter build apk`

#### 4. iOS build errors (macOS)
**Solution:**
```bash
cd ios
pod install
cd ..
flutter clean
flutter build ios
```

#### 5. Firebase errors
**Note:** Firebase has been disabled in this academic version. If you see Firebase-related errors:
- Ensure all Firebase imports are commented out in `main.dart`
- Check that Google services are disabled in `build.gradle`

#### 6. Package conflicts
**Solution:**
```bash
flutter clean
flutter pub cache repair
flutter pub get
```

---

## 🧪 Development Mode

### Hot Reload
While the app is running, you can make changes to the code and press:
- **`r`** - Hot reload (fast, preserves state)
- **`R`** - Hot restart (slower, resets state)
- **`q`** - Quit

### Debug Mode
```bash
flutter run --debug
```

### Profile Mode (for performance testing)
```bash
flutter run --profile
```

---

## 📦 Package Information

### Main Dependencies

| Package | Purpose |
|---------|---------|
| drift | Local SQL database |
| sqlite3_flutter_libs | SQLite libraries |
| fl_chart | Data visualization |
| shared_preferences | App settings storage |
| local_auth | Biometric authentication |
| easy_localization | Multi-language support |
| provider | State management |

### Disabled Dependencies (Academic Version)

The following packages are commented out:
- firebase_core
- firebase_auth
- cloud_firestore
- google_sign_in
- in_app_purchase

---

## 🎯 Recommended Development Workflow

1. **Make changes** to the code
2. **Hot reload** (`r`) to see changes instantly
3. **Test** functionality on emulator/device
4. **Build release** version for submission
5. **Test release** build on physical device

---

## 📊 Performance Tips

### Reduce Build Size
```bash
flutter build apk --split-per-abi
```
This creates separate APKs for different CPU architectures, reducing individual file sizes.

### Analyze App Size
```bash
flutter build apk --analyze-size
```

### Check for Unused Code
```bash
flutter analyze
```

---

## 🔍 Useful Commands

```bash
# Check Flutter installation
flutter doctor -v

# List connected devices
flutter devices

# Clean build cache
flutter clean

# Update Flutter
flutter upgrade

# Check for outdated packages
flutter pub outdated

# Generate app icons
flutter pub run flutter_launcher_icons:main

# Run tests
flutter test

# Format code
flutter format .

# Analyze code
flutter analyze
```

---

## 📝 Notes for Academic Submission

### What to Submit:

1. **Source Code**: Entire `/app/budget` directory
2. **APK File**: Built release APK (if requested)
3. **Documentation**: README_STUDENT.md and this guide
4. **Screenshots**: App screens showing key features
5. **Demo Video**: (if required)

### Building for Submission:

```bash
# Navigate to project
cd /app/budget

# Clean previous builds
flutter clean

# Get dependencies
flutter pub get

# Build release APK
flutter build apk --release

# APK will be at:
# /app/budget/build/app/outputs/flutter-apk/app-release.apk
```

---

## 🆘 Getting Help

### Official Resources
- Flutter Documentation: https://flutter.dev/docs
- Dart Documentation: https://dart.dev/guides
- Flutter Community: https://flutter.dev/community

### Debug Information
```bash
# Get detailed error information
flutter run --verbose

# Check logs
flutter logs
```

---

## ✅ Pre-Submission Checklist

- [ ] Code compiles without errors
- [ ] App runs on emulator/device
- [ ] All major features are functional
- [ ] No critical bugs or crashes
- [ ] Release APK builds successfully
- [ ] App has been tested on physical device
- [ ] Documentation is complete
- [ ] Screenshots/demo video prepared (if required)

---

**Project:** Ledgerly - Smart Expense Tracking  
**Version:** 1.0.0  
**Framework:** Flutter  
**Last Updated:** January 2025
