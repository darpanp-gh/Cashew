# Ledgerly - Smart Expense Tracking App

<div align="center">
  <h3>A Mobile App Development Course Project</h3>
  <p><em>Smart expense tracking, simplified</em></p>
</div>

---

## 📱 About This Project

**Ledgerly** is a comprehensive expense tracking application developed as part of a Mobile App Development course. This cross-platform mobile app demonstrates modern development practices, local database management, and elegant UI/UX design.

### 🎯 Project Objectives

- Demonstrate proficiency in cross-platform mobile development using Flutter
- Implement local database management with Drift SQL
- Apply Material Design principles and custom theming
- Create an intuitive and responsive user interface
- Develop complex features like multi-currency support and data visualization

---

## ✨ Key Features

### 💸 Budget Management
- Create custom budgets with flexible time periods (daily, weekly, monthly, custom)
- Set spending limits for different categories
- Track budget history and analyze spending patterns
- Create financial goals and monitor progress

### 💰 Transaction Management
- Support for multiple transaction types (expenses, income, subscriptions, debts)
- Custom categories with icon selection
- Quick transaction entry with auto-suggestions
- Advanced search and filter capabilities
- Bulk selection and editing

### 💱 Multi-Currency Support
- Manage multiple accounts with different currencies
- Automatic currency conversion with up-to-date rates
- Seamless account switching

### 📊 Data Visualization
- Interactive charts and graphs
- Spending pattern analysis
- Category breakdown visualization
- Financial trends over time

### 🔒 Security Features
- Biometric authentication (fingerprint/face recognition)
- Local data storage for privacy
- Secure transaction data

### 🎨 Modern UI/UX
- Material You design implementation
- Light and dark mode support
- Custom accent colors
- Customizable home screen layout
- Responsive design for various screen sizes

### 💾 Data Management
- CSV import/export functionality
- Database backup and restore
- Data migration tools

---

## 🛠️ Technical Stack

| Technology | Purpose |
|------------|---------|
| **Flutter** | Cross-platform framework |
| **Dart** | Programming language |
| **Drift (Moor)** | Local SQL database |
| **SQLite** | Database engine |
| **Material Design** | UI/UX framework |
| **Provider** | State management |
| **Easy Localization** | Multi-language support |

---

## 📐 Architecture

### Database Schema
- Uses Drift for type-safe SQL database operations
- Schema versioning and migration support
- Efficient query optimization

### State Management
- Provider pattern for reactive state management
- SharedPreferences for app settings
- Global state for app-wide data

### Design Pattern
- Material Design 3 (Material You)
- Responsive layouts for phones and tablets
- Custom theme system with dynamic colors

---

## 🚀 Getting Started

### Prerequisites
- Flutter SDK (3.0+)
- Android Studio / VS Code
- Android SDK (for Android builds)
- Xcode (for iOS builds, macOS only)

### Installation

1. **Clone the repository**
   ```bash
   cd /app/budget
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Run the app**
   ```bash
   flutter run
   ```

### Building

**Android APK:**
```bash
flutter build apk --release
```

**Android App Bundle:**
```bash
flutter build appbundle --release
```

**iOS (requires macOS):**
```bash
flutter build ipa
```

---

## 📂 Project Structure

```
budget/
├── lib/
│   ├── main.dart                 # App entry point
│   ├── database/                 # Drift database files
│   │   └── tables.dart           # Database schema
│   ├── pages/                    # App screens/pages
│   ├── widgets/                  # Reusable UI components
│   ├── struct/                   # Data structures & utilities
│   └── colors.dart               # Theme and color definitions
├── android/                      # Android-specific files
├── ios/                          # iOS-specific files
├── assets/                       # Images, fonts, icons
└── pubspec.yaml                  # Dependencies
```

---

## 🎓 Learning Outcomes

Through this project, the following skills were demonstrated:

1. **Mobile Development**
   - Cross-platform app development with Flutter
   - Platform-specific configurations (Android & iOS)
   - Responsive UI design

2. **Database Management**
   - SQL database design and implementation
   - CRUD operations
   - Data migrations and versioning

3. **State Management**
   - Reactive programming with Provider
   - Persistent storage with SharedPreferences
   - Global state management

4. **UI/UX Design**
   - Material Design implementation
   - Custom theming and styling
   - Accessibility considerations

5. **Software Engineering**
   - Clean code practices
   - Modular architecture
   - Version control

---

## 📊 Features Demonstration

### Core Functionality
- ✅ Create and manage transactions
- ✅ Organize expenses by category
- ✅ Set and track budgets
- ✅ Visualize spending with charts
- ✅ Multi-currency support
- ✅ Data export (CSV format)
- ✅ Biometric authentication
- ✅ Light/dark theme support

### Advanced Features
- ✅ Custom budget periods
- ✅ Recurring transactions
- ✅ Category icons and customization
- ✅ Search and filtering
- ✅ Spending goals
- ✅ Historical data analysis

---

## 🔧 Configuration

The app uses local storage exclusively for academic purposes. Firebase integration has been disabled.

### App Configuration
- **Package Name:** com.ledgerly.tracker
- **Version:** 1.0.0
- **Min SDK:** 23 (Android 6.0)
- **Target SDK:** 34 (Android 14)

---

## 📝 Notes

- This is an academic project for educational purposes
- All data is stored locally on the device
- No external cloud services are used
- Premium/subscription features have been disabled

---

## 📄 License

See LICENSE file for details.

---

## 👨‍💻 Development Information

**Course:** Mobile App Development  
**Framework:** Flutter 3.0+  
**Database:** Drift (SQL)  
**Version:** 1.0.0 (Educational Release)  
**Date:** January 2025  

---

## 🙏 Acknowledgments

This project is based on the open-source Cashew app by James Kokoska. The app has been rebranded and modified for academic purposes with proper attribution to the original creator.

**Original Project:** [Cashew on GitHub](https://github.com/jameskokoska/Cashew)

---

<div align="center">
  <p><strong>Ledgerly</strong> - Smart expense tracking, simplified</p>
  <p><em>A Mobile App Development Course Project</em></p>
</div>
