# 📥 How to Download Ledgerly to Your Computer

## Quick Download Methods

---

## Method 1: Create ZIP File (Recommended)

### Create Archive
```bash
cd /app
tar -czf ledgerly-complete.tar.gz budget/
# or
zip -r ledgerly-complete.zip budget/
```

### Then Download
- The file will be at `/app/ledgerly-complete.tar.gz` or `.zip`
- Download it through your file manager or terminal
- Extract on your local machine

---

## Method 2: Direct Folder Copy

If you have file system access:
1. Navigate to `/app/budget/`
2. Copy the entire `budget` folder
3. Paste to your computer at:
   - Windows: `C:\Users\YourName\AndroidStudioProjects\ledgerly`
   - Mac: `~/AndroidStudioProjects/ledgerly`
   - Linux: `~/AndroidStudioProjects/ledgerly`

---

## Method 3: Git Repository (If Available)

If this is a git repo:
```bash
cd /app/budget
git init
git add .
git commit -m "Ledgerly rebranded app"

# Then push to GitHub/GitLab or clone to your machine
```

---

## After Download

### File Structure You Should Have

```
ledgerly/  (or budget/)
├── android/
├── ios/
├── lib/
├── assets/
├── pubspec.yaml
├── README_LEDGERLY.md
├── ANDROID_STUDIO_SETUP.md
├── QUICK_START_ANDROID_STUDIO.md
└── [all other documentation files]
```

### Verify Files

Check these key files exist:
- [ ] `pubspec.yaml`
- [ ] `lib/main.dart`
- [ ] `android/` folder
- [ ] `ios/` folder
- [ ] All `.md` documentation files

---

## Next Steps

Once downloaded:

1. **Open in Android Studio**
   - Follow `QUICK_START_ANDROID_STUDIO.md`

2. **Install Dependencies**
   ```bash
   cd ledgerly
   flutter pub get
   ```

3. **Run the App**
   - Open in Android Studio
   - Click Run ▶️

---

## File Size

Expected size: ~50-100 MB (depending on generated files)

If larger, you may want to clean first:
```bash
cd /app/budget
flutter clean
# Then create archive
```

---

## Troubleshooting Download

### If ZIP/TAR fails
- Try smaller chunks
- Download folders separately
- Use git if available

### If files are missing
- Verify `/app/budget/` path is correct
- Check all subfolders are included
- Ensure hidden files are copied (starting with .)

---

## Ready to Open in Android Studio?

See: `QUICK_START_ANDROID_STUDIO.md` for the next steps!
