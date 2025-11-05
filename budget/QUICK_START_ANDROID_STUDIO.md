# ⚡ Quick Start - Running Ledgerly in Android Studio

## 🎯 Fast Setup (10 Minutes)

### ✅ Pre-flight Checklist

- [ ] Android Studio installed
- [ ] Physical Android device OR emulator ready
- [ ] Project files copied to your computer

---

## 🚀 5 Simple Steps

### 1️⃣ Install Flutter Plugin (2 minutes)

**In Android Studio:**
1. File → Settings → Plugins
2. Search: "Flutter"
3. Click "Install"
4. Restart Android Studio

### 2️⃣ Install Flutter SDK (3 minutes)

**Download & Install:**
- Windows: https://docs.flutter.dev/get-started/install/windows
- Mac: https://docs.flutter.dev/get-started/install/macos
- Linux: https://docs.flutter.dev/get-started/install/linux

**Quick Install (Mac/Linux):**
```bash
cd ~/development
git clone https://github.com/flutter/flutter.git -b stable
export PATH="$PATH:`pwd`/flutter/bin"
flutter doctor
```

### 3️⃣ Open Project (1 minute)

**In Android Studio:**
1. File → Open
2. Navigate to your `budget` folder
3. Click "OK"
4. Wait for indexing to complete

### 4️⃣ Get Dependencies (1 minute)

**In Android Studio Terminal (Alt+F12):**
```bash
flutter pub get
```

### 5️⃣ Run! (2 minutes)

**In Android Studio:**
1. Select device from dropdown (top toolbar)
   - If no device: Tools → Device Manager → Create Device
2. Click green ▶️ Run button
3. Wait for build (first time: 3-5 mins)
4. App launches! 🎉

---

## 📱 Device Setup

### Option A: Emulator (Easiest)

1. Tools → Device Manager
2. Create Virtual Device → Pixel 5
3. Download system image (Android 13)
4. Click ▶️ to start emulator

### Option B: Physical Device

1. **On Phone:** Settings → About → Tap "Build Number" 7 times
2. **Enable:** Settings → Developer Options → USB Debugging
3. **Connect:** USB cable to computer
4. **Verify:** Should appear in device dropdown

---

## ⚡ Quick Commands

```bash
# In Android Studio Terminal (Alt+F12 or Option+F12)

flutter pub get        # Get dependencies
flutter run           # Run app
flutter clean         # Clean build
flutter doctor        # Check setup
```

---

## 🐛 Quick Fixes

### "Flutter SDK not found"
```bash
# Set Flutter path in Android Studio:
# File → Settings → Languages & Frameworks → Flutter
# Point to where you installed Flutter
```

### "No devices available"
- Start emulator: Tools → Device Manager → Play
- Or connect phone via USB

### "Gradle build failed"
```bash
flutter clean
flutter pub get
flutter run
```

### "Android licenses not accepted"
```bash
flutter doctor --android-licenses
# Type 'y' to accept all
```

---

## 🎉 Success Indicators

✅ You should see:
- Ledgerly splash screen
- Main expense tracking screen
- No "Cashew" text anywhere
- All features working

---

## 📚 Need More Detail?

- **Complete guide**: `ANDROID_STUDIO_SETUP.md`
- **Troubleshooting**: `BUILD_AND_TEST_GUIDE.md`
- **Testing**: `VERIFICATION_CHECKLIST.md`

---

## ⏱️ Timeline

| Step | Time | Action |
|------|------|--------|
| 0 | 2 min | Install Flutter plugin |
| 1 | 3 min | Install Flutter SDK |
| 2 | 1 min | Open project |
| 3 | 1 min | Run flutter pub get |
| 4 | 5 min | First build & run |
| **Total** | **12 min** | **App running!** |

---

## 🔥 Hot Reload (Flutter's Superpower!)

Once app is running:
1. Make any code change
2. Save file (Ctrl+S / Cmd+S)
3. Press `r` in terminal
4. See changes instantly! ⚡

No need to rebuild!

---

## 💡 Pro Tips

1. **Keep emulator running** between sessions
2. **Use hot reload** (`r`) instead of full restart
3. **First build is slow** (3-5 mins), then fast (30 secs)
4. **Check `flutter doctor`** if issues arise

---

## 🆘 Still Stuck?

### Verify Flutter Setup
```bash
flutter doctor -v
```
All items should have ✓ checkmarks

### Clean Everything
```bash
flutter clean
flutter pub get
flutter run
```

### Check Files Exist
- [ ] `pubspec.yaml` in project root
- [ ] `lib/main.dart` exists
- [ ] `android/` folder exists

---

## 📍 Where to Get Help

1. **Full setup guide**: Open `ANDROID_STUDIO_SETUP.md`
2. **Flutter docs**: https://docs.flutter.dev
3. **Flutter Discord**: https://discord.gg/flutter

---

**You're just 10 minutes away from seeing Ledgerly running! 🚀**

Start with Step 1 above and work your way down!
