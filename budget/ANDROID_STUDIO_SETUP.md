# 🚀 Running Ledgerly in Android Studio - Complete Guide

## Step-by-Step Setup Instructions

---

## ✅ Prerequisites Check

Before starting, verify you have:
- [x] Android Studio installed
- [ ] Flutter SDK installed
- [ ] Android device or emulator

---

## 📥 Step 1: Download Your Project

### Method A: If you have terminal access to the server
```bash
# Create a zip of the budget folder
cd /app
tar -czf ledgerly-app.tar.gz budget/

# Download this file to your local machine
```

### Method B: Manual file copy
Copy the entire `/app/budget/` folder to your local machine.

**Recommended location:**
- Windows: `C:\Users\YourName\AndroidStudioProjects\ledgerly`
- Mac: `~/AndroidStudioProjects/ledgerly`
- Linux: `~/AndroidStudioProjects/ledgerly`

---

## 🛠️ Step 2: Install Flutter SDK (If Not Already Installed)

### Windows

1. **Download Flutter**
   - Visit: https://docs.flutter.dev/get-started/install/windows
   - Download Flutter SDK (latest stable)
   - Extract to: `C:\src\flutter` (recommended)

2. **Add to PATH**
   - Open "Environment Variables"
   - Add to PATH: `C:\src\flutter\bin`
   - Open new terminal and verify:
   ```cmd
   flutter --version
   ```

3. **Run Flutter Doctor**
   ```cmd
   flutter doctor
   ```

### macOS

1. **Download Flutter**
   ```bash
   cd ~/development
   git clone https://github.com/flutter/flutter.git -b stable
   ```

2. **Add to PATH**
   ```bash
   export PATH="$PATH:`pwd`/flutter/bin"
   echo 'export PATH="$PATH:$HOME/development/flutter/bin"' >> ~/.zshrc
   ```

3. **Run Flutter Doctor**
   ```bash
   flutter doctor
   ```

### Linux

1. **Download Flutter**
   ```bash
   cd ~/development
   git clone https://github.com/flutter/flutter.git -b stable
   ```

2. **Add to PATH**
   ```bash
   export PATH="$PATH:$HOME/development/flutter/bin"
   echo 'export PATH="$PATH:$HOME/development/flutter/bin"' >> ~/.bashrc
   ```

3. **Run Flutter Doctor**
   ```bash
   flutter doctor
   ```

---

## ⚙️ Step 3: Configure Android Studio for Flutter

### Install Flutter & Dart Plugins

1. **Open Android Studio**

2. **Go to Plugins**
   - File → Settings (Windows/Linux)
   - Android Studio → Preferences (macOS)
   - Click "Plugins"

3. **Search and Install**
   - Search: "Flutter"
   - Click "Install"
   - This will also install the Dart plugin
   - Click "Restart IDE"

### Configure Flutter SDK Path

1. **After restart, configure SDK**
   - File → Settings → Languages & Frameworks → Flutter
   - Set "Flutter SDK path" to where you installed Flutter
   - Windows: `C:\src\flutter`
   - macOS/Linux: `~/development/flutter`

2. **Verify Setup**
   - Open Terminal in Android Studio
   - Run: `flutter doctor`
   - Should show Flutter is properly configured

---

## 📂 Step 4: Open Your Ledgerly Project

### Method 1: Via Android Studio

1. **Open Project**
   - File → Open
   - Navigate to where you copied the `budget` folder
   - Select the `budget` folder
   - Click "OK"

2. **Wait for Indexing**
   - Android Studio will index the project
   - This may take 2-5 minutes first time
   - You'll see progress at the bottom

### Method 2: Via Terminal

```bash
# Navigate to project
cd /path/to/budget

# Get dependencies
flutter pub get

# Open in Android Studio
studio .  # or 'open -a "Android Studio" .' on macOS
```

---

## 🔧 Step 5: Resolve Dependencies

### Get Flutter Packages

1. **Open Terminal in Android Studio** (Alt+F12 / Option+F12)

2. **Run:**
   ```bash
   flutter pub get
   ```

3. **Wait for completion**
   - Should see "Got dependencies!"
   - May take 1-2 minutes

### Fix Any Issues

If you see errors:

```bash
# Clean project
flutter clean

# Get dependencies again
flutter pub get

# If drift/database issues:
flutter pub run build_runner build --delete-conflicting-outputs
```

---

## 📱 Step 6: Set Up Device/Emulator

### Option A: Use Android Emulator

1. **Open AVD Manager**
   - Tools → Device Manager
   - Or click AVD icon in toolbar

2. **Create Virtual Device**
   - Click "Create Virtual Device"
   - Choose: Pixel 5 (recommended)
   - System Image: Android 13 (API 33) or newer
   - Click "Finish"

3. **Start Emulator**
   - Click ▶️ (Play) button next to device
   - Wait for emulator to boot (1-2 minutes)

### Option B: Use Physical Device

1. **Enable Developer Mode on Android Phone**
   - Go to Settings → About Phone
   - Tap "Build Number" 7 times
   - Developer Options now enabled

2. **Enable USB Debugging**
   - Settings → Developer Options
   - Turn on "USB Debugging"

3. **Connect to Computer**
   - Connect phone via USB cable
   - On phone: Allow USB debugging prompt
   - In Android Studio: Device should appear in dropdown

4. **Verify Connection**
   ```bash
   flutter devices
   ```
   Should show your device

---

## ▶️ Step 7: Run the App!

### Method 1: Using Android Studio UI

1. **Select Device**
   - Top toolbar → Device dropdown
   - Select your emulator or physical device

2. **Click Run**
   - Click green ▶️ (Run) button
   - Or press Shift+F10 (Windows/Linux)
   - Or press Control+R (macOS)

3. **Wait for Build**
   - First build: 3-5 minutes
   - Subsequent builds: 30-60 seconds
   - Watch progress in bottom panel

### Method 2: Using Terminal

```bash
# List available devices
flutter devices

# Run on specific device
flutter run

# Or run in release mode
flutter run --release
```

### Expected Output

```
Launching lib/main.dart on Pixel 5 in debug mode...
Running Gradle task 'assembleDebug'...
✓ Built build/app/outputs/flutter-apk/app-debug.apk.
Installing build/app/outputs/flutter-apk/app-debug.apk...
Syncing files to device Pixel 5...
Flutter run key commands.
r Hot reload. 🔥
R Hot restart.
h List all available commands.
d Detach (terminate "flutter run" but leave application running).
c Clear the screen
q Quit (terminate the application on the device).
```

---

## 🎉 Step 8: Test the App

### Initial Launch

When the app first launches:
1. You'll see the Ledgerly splash screen
2. App will initialize database
3. Main screen will appear

### Test Basic Features

- [ ] Create a new transaction
- [ ] View transaction list
- [ ] Create a budget
- [ ] Check charts
- [ ] Export data (should say "Ledgerly Data File")

### Verify Branding

- [ ] App name shows "Ledgerly"
- [ ] No "Cashew" text visible
- [ ] All features working

---

## 🔥 Using Hot Reload

### While App is Running

**Make a change to the code:**
1. Open any `.dart` file
2. Make a small change (e.g., change text)
3. Save the file (Ctrl+S / Cmd+S)
4. Press `r` in terminal or click Hot Reload button
5. Changes appear instantly!

**This is Flutter's superpower - see changes in seconds!**

---

## 🐛 Troubleshooting Common Issues

### Issue 1: "Flutter SDK not found"

**Solution:**
```bash
# Verify Flutter is in PATH
flutter --version

# If not, add to PATH and restart Android Studio
```

### Issue 2: "Gradle build failed"

**Solution:**
```bash
cd /path/to/budget
flutter clean
flutter pub get
flutter run
```

### Issue 3: "No devices available"

**Solution:**
- Start an emulator: Tools → Device Manager → Start
- Or connect physical device with USB debugging enabled
- Verify: `flutter devices`

### Issue 4: "Could not resolve dependencies"

**Solution:**
```bash
# Delete these folders
rm -rf .dart_tool/
rm pubspec.lock

# Get dependencies again
flutter pub get
```

### Issue 5: "Drift/Database errors"

**Solution:**
```bash
# Rebuild generated files
flutter pub run build_runner build --delete-conflicting-outputs
```

### Issue 6: "Android licenses not accepted"

**Solution:**
```bash
flutter doctor --android-licenses
# Accept all licenses (type 'y')
```

### Issue 7: "Build takes too long"

**First build is slow (3-5 minutes). Speed up:**
```bash
# Enable Gradle daemon
echo "org.gradle.daemon=true" >> android/gradle.properties

# Increase memory
echo "org.gradle.jvmargs=-Xmx4g" >> android/gradle.properties
```

---

## 🎯 Quick Commands Reference

```bash
# Get dependencies
flutter pub get

# Clean project
flutter clean

# List devices
flutter devices

# Run app
flutter run

# Run in release mode
flutter run --release

# Build APK
flutter build apk

# Build for release
flutter build apk --release

# Check Flutter setup
flutter doctor

# Analyze code
flutter analyze
```

---

## 📊 Android Studio Shortcuts

### Useful Shortcuts

| Action | Windows/Linux | macOS |
|--------|--------------|-------|
| Run app | Shift+F10 | Control+R |
| Hot reload | Ctrl+\ | Cmd+\ |
| Stop app | Ctrl+F2 | Cmd+F2 |
| Find | Ctrl+F | Cmd+F |
| Save all | Ctrl+S | Cmd+S |
| Terminal | Alt+F12 | Option+F12 |
| Format code | Ctrl+Alt+L | Cmd+Option+L |

---

## 🚀 Building APK for Testing

### Debug APK (for testing)
```bash
flutter build apk --debug
```
Location: `build/app/outputs/flutter-apk/app-debug.apk`

### Release APK (for distribution)
```bash
flutter build apk --release
```
Location: `build/app/outputs/flutter-apk/app-release.apk`

### Install on Device
```bash
# Via ADB
adb install build/app/outputs/flutter-apk/app-debug.apk

# Or copy APK to phone and install manually
```

---

## ✅ Verification Checklist

After successfully running:

- [ ] App launches without errors
- [ ] Ledgerly name appears correctly
- [ ] Can create transactions
- [ ] Can view transaction list
- [ ] Charts display properly
- [ ] No "Cashew" branding visible
- [ ] Hot reload works
- [ ] All features functional

---

## 💡 Pro Tips

### Speed Up Development

1. **Use Hot Reload** (instead of full restart)
   - Press `r` in terminal after code changes
   - Nearly instant updates!

2. **Keep Emulator Running**
   - Don't close between sessions
   - Reconnects automatically

3. **Use Flutter Inspector**
   - View → Tool Windows → Flutter Inspector
   - Debug widget layout issues

4. **Enable Auto-save**
   - File → Settings → Appearance & Behavior → System Settings
   - Enable "Save files automatically"

### Optimize Performance

1. **Use Profile Mode** (for performance testing)
   ```bash
   flutter run --profile
   ```

2. **Analyze Performance**
   - View → Tool Windows → Flutter Performance
   - Check for jank and dropped frames

---

## 📱 Next Steps After Running

1. **Test thoroughly** using `VERIFICATION_CHECKLIST.md`
2. **Make any customizations** you want
3. **Build release APK** when satisfied
4. **Install on real device** for final testing

---

## 🆘 Still Having Issues?

### Check These

1. **Flutter Doctor**
   ```bash
   flutter doctor -v
   ```
   Should show all ✓ checkmarks

2. **Project Structure**
   - Ensure `pubspec.yaml` exists
   - Ensure `lib/main.dart` exists
   - Ensure `android/` folder exists

3. **Android Studio Plugin**
   - Verify Flutter plugin is installed
   - Restart Android Studio

4. **Clean Everything**
   ```bash
   flutter clean
   cd android && ./gradlew clean && cd ..
   flutter pub get
   flutter run
   ```

---

## 🎉 Success!

Once you see the Ledgerly app running on your device/emulator:
- You can make changes and see them instantly with hot reload
- Test all features
- Build APK for sharing
- Continue development

**Congratulations! You're now running Ledgerly in Android Studio! 🚀**

---

**Need more help?** Check these files:
- `BUILD_AND_TEST_GUIDE.md` - General build instructions
- `VERIFICATION_CHECKLIST.md` - Testing checklist
- `README_LEDGERLY.md` - Project overview
