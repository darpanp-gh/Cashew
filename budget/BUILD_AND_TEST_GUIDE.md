# Ledgerly - Build and Test Guide

## 🛠️ Prerequisites

Before building the app, ensure you have:
- Flutter SDK installed (version 3.0.0 or higher)
- Android Studio with Android SDK
- Xcode (for iOS builds, macOS only)
- Physical device or emulator/simulator

## 📱 Building the App

### Android Build

#### 1. Debug Build (for testing)
```bash
cd /app/budget
flutter pub get
flutter build apk --debug
```
Output: `build/app/outputs/flutter-apk/app-debug.apk`

#### 2. Release Build (for distribution)
```bash
flutter build apk --release
```
Output: `build/app/outputs/flutter-apk/app-release.apk`

#### 3. App Bundle (for Play Store)
```bash
flutter build appbundle --release
```
Output: `build/app/outputs/bundle/release/app-release.aab`

### iOS Build (macOS only)

#### 1. Debug Build
```bash
cd /app/budget
flutter pub get
flutter build ios --debug
```

#### 2. Release Build
```bash
flutter build ios --release
```

## 📲 Installing on Device

### Android

#### Via USB (ADB)
```bash
# Enable USB debugging on your Android device
adb devices
adb install build/app/outputs/flutter-apk/app-debug.apk
```

#### Via File Transfer
1. Copy `app-debug.apk` to your device
2. Enable "Install from Unknown Sources" in Settings
3. Tap the APK file to install

### iOS

#### Via Xcode
1. Open `ios/Runner.xcworkspace` in Xcode
2. Connect your iOS device
3. Select your device as the target
4. Click Run (▶️)

## 🧪 Testing Checklist

### Installation Tests
- [ ] App installs successfully
- [ ] App icon displays correctly
- [ ] App name shows as "Ledgerly"

### Launch Tests
- [ ] App launches without crashes
- [ ] Splash screen displays correctly
- [ ] No error messages on first launch

### Feature Tests

#### Core Functionality
- [ ] Create new transaction (expense/income)
- [ ] Edit existing transaction
- [ ] Delete transaction
- [ ] View transaction list
- [ ] Filter transactions by date
- [ ] Search transactions

#### Accounts
- [ ] Create new account
- [ ] Edit account
- [ ] Delete account
- [ ] Switch between accounts
- [ ] View account balance

#### Categories
- [ ] Create new category
- [ ] Edit category
- [ ] Delete category
- [ ] Assign icon to category
- [ ] Assign color to category

#### Budgets
- [ ] Create new budget
- [ ] Edit budget
- [ ] Delete budget
- [ ] View budget progress
- [ ] Budget notifications (if enabled)

#### Charts & Analytics
- [ ] View spending chart
- [ ] View category breakdown
- [ ] View time-based analytics
- [ ] Export chart data

#### Data Management
- [ ] Export data (SQLite/SQL format)
- [ ] Import data
- [ ] Verify exported file name contains "Ledgerly"

#### Settings
- [ ] Change theme (light/dark)
- [ ] Change currency
- [ ] Set biometric lock
- [ ] Configure notifications
- [ ] Access app information

### Branding Verification
- [ ] No "Cashew" text appears anywhere
- [ ] App name is "Ledgerly" throughout
- [ ] Package name is `com.ledgerly.tracker`

### Performance Tests
- [ ] Smooth scrolling in transaction list
- [ ] Fast app startup
- [ ] No lag in chart rendering
- [ ] Database operations are responsive

## 🐛 Common Issues

### Build Errors

**Issue**: `Gradle build failed`
```bash
# Solution: Clean build
cd /app/budget
flutter clean
flutter pub get
flutter build apk
```

**Issue**: `CocoaPods not installed` (iOS)
```bash
# Solution: Install CocoaPods
sudo gem install cocoapods
cd ios
pod install
```

**Issue**: `Signing certificate error` (iOS)
```bash
# Solution: Configure signing in Xcode
# Open ios/Runner.xcworkspace
# Go to Runner > Signing & Capabilities
# Select your development team
```

### Runtime Errors

**Issue**: App crashes on launch
- Check logs: `flutter logs`
- Verify database initialization
- Check permissions in manifest

**Issue**: Features not working
- Verify all dependencies installed
- Check device permissions
- Review console logs

## 📊 Performance Monitoring

### During Testing
```bash
# View real-time logs
flutter logs

# Run with performance overlay
flutter run --profile
```

### Memory Profiling
```bash
# Use Flutter DevTools
flutter pub global activate devtools
flutter pub global run devtools
```

## 🔍 Debug Mode

### Enable Debug Features
In `main.dart`, set:
```dart
bool enableDevicePreview = true && kDebugMode;
```

### View Debug Banner
The debug banner indicates you're in debug mode. This is normal during development.

## ✅ Test Sign-Off

### Before Submitting Project
- [ ] All core features tested ✓
- [ ] No crashes or critical bugs ✓
- [ ] Branding verified ✓
- [ ] Performance acceptable ✓
- [ ] Data export/import works ✓

### Test Environment
- **Device**: _____________
- **OS Version**: _____________
- **Build Type**: Debug / Release
- **Date Tested**: _____________
- **Tester**: _____________

### Test Results
- **Pass**: _____ tests
- **Fail**: _____ tests
- **Notes**: _________________________________

## 📝 Notes

### Important Paths
- **Android APK**: `build/app/outputs/flutter-apk/`
- **Android Bundle**: `build/app/outputs/bundle/release/`
- **iOS Build**: `build/ios/iphoneos/`

### Testing Tips
1. Always test on physical device if possible
2. Test both light and dark themes
3. Test with different currencies
4. Test data import/export thoroughly
5. Verify all permissions work correctly

### Academic Submission
For academic submission, include:
- APK file (Android) or IPA file (iOS)
- Screenshots of the app
- This testing documentation
- REBRANDING_CHANGES.md
- Any test results

---

**Status**: Ready for build and test  
**Framework**: Flutter  
**Target Platforms**: Android, iOS  
**Last Updated**: Current session
