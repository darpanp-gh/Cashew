# Ledgerly - Rebranding Summary

## New App Identity

**App Name:** Ledgerly
**Tagline:** Smart expense tracking, simplified
**Package ID:** com.ledgerly.tracker
**Version:** 1.0.0+1

## Branding Details

### Logo Concept
- **Design:** Minimalist "L" shape forming a ledger book with clean lines
- **Primary Color:** Navy Blue (#2C3E50)
- **Accent Color:** Soft Cyan (#3498DB)
- **Style:** Professional, minimal, elegant

### Academic Project Description
> "A comprehensive expense tracking application developed as part of a Mobile App Development course. Built with Flutter, this app demonstrates cross-platform mobile development skills, local database management with Drift SQL, and modern Material Design UI/UX principles. Features include budget management, transaction categorization, multi-currency support, and interactive data visualization."

## Technical Changes Made

### 1. Core Identity Files
- ✅ `pubspec.yaml` - Updated name to "ledgerly", description, version 1.0.0
- ✅ `AndroidManifest.xml` - Changed package to com.ledgerly.tracker, label to "Ledgerly"
- ✅ `build.gradle` - Updated applicationId to com.ledgerly.tracker
- ✅ `lib/struct/languageMap.dart` - Changed globalAppName to "Ledgerly"
- ✅ `lib/main.dart` - Updated app title to "Ledgerly"

### 2. Firebase Integration
- ✅ Commented out Firebase dependencies in pubspec.yaml
- ✅ Commented out Firebase initialization in main.dart
- ✅ Disabled Google services plugin in build.gradle
- ✅ Removed Firebase deep link URLs from AndroidManifest

### 3. Branding References
- ✅ Updated all "Cashew" references to "Ledgerly" in code
- ✅ Updated export file names from "cashew-" to "ledgerly-"
- ✅ Disabled premium/pro features (academic version)
- ✅ Updated app URLs and links

### 4. Documentation
- ✅ Created new README.md for student project
- ✅ Removed promotional materials references
- ✅ Added academic project documentation

## Files to Modify

1. `/app/budget/pubspec.yaml`
2. `/app/budget/android/app/src/main/AndroidManifest.xml`
3. `/app/budget/android/app/build.gradle`
4. `/app/budget/lib/struct/languageMap.dart`
5. `/app/budget/lib/main.dart`
6. `/app/README.md`

## App Icon & Splash Screen

### Recommended Icon Design
For your app icon, create a simple design:
- Navy blue (#2C3E50) background
- White or cyan "L" letter in a modern sans-serif font
- Optional: Subtle ledger lines in the background
- Keep it minimal and professional

### Tools to Create Icon:
1. **Canva** (free, easy to use)
2. **Figma** (professional, free tier)
3. **Adobe Express** (quick icon maker)

### To Update App Icons:
1. Create your icon (512x512px PNG)
2. Save it as `/app/budget/assets/icon/icon.png`
3. Run: `flutter pub run flutter_launcher_icons:main`

## Features Disabled for Academic Version

- ❌ Firebase Authentication
- ❌ Cloud Firestore sync
- ❌ Google Sign-In
- ❌ In-app purchases (Pro features)
- ❌ External deep links to cashewapp.web.app
- ✅ Local database (Drift SQL) - ACTIVE
- ✅ All core expense tracking features - ACTIVE
- ✅ Biometric lock - ACTIVE
- ✅ CSV import/export - ACTIVE

## Building the App

### Android APK
```bash
cd /app/budget
flutter pub get
flutter build apk --release
```

### Android App Bundle
```bash
flutter build appbundle --release
```

## Project Submission Notes

**Course:** Mobile App Development
**Framework:** Flutter 3.0+
**Database:** Drift (SQL)
**Architecture:** Material Design with custom theming

**Key Features to Highlight:**
1. Local database management with Drift SQL
2. Cross-platform compatibility (Android/iOS)
3. Material You design implementation
4. Multi-currency support
5. Data visualization with charts
6. Biometric authentication
7. CSV data import/export

## Original Attribution

This is a rebranded educational version. Original app: Cashew by James Kokoska
GitHub: https://github.com/jameskokoska/Cashew
License: See LICENSE file

---

**Created:** January 2025
**Version:** 1.0.0 (Educational Release)
