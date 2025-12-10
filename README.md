# 💰 Splitter - Expense Splitting & Personal Finance Tracker

<div align="center">

![Flutter](https://img.shields.io/badge/Flutter-3.38.3-02569B?logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-3.0+-0175C2?logo=dart&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?logo=firebase&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-green.svg)

**A beautiful, modern expense splitting application built with Flutter (Cupertino style) for seamless group expense management and personal finance tracking.**

[Features](#-features) • [Screenshots](#-screenshots) • [Installation](#-installation) • [Usage](#-usage) • [Tech Stack](#-tech-stack) • [Project Structure](#-project-structure)

</div>

---

## 📱 About

Splitter is a sophisticated mobile application designed to simplify expense splitting among friends, roommates, and groups. Whether you're managing a trip, tracking bachelor mess expenses, or splitting bills with friends, Splitter makes it easy to track who paid what and calculate settlements automatically.

### Key Highlights

- 🎨 **Beautiful iOS-style UI** - Built with Cupertino design following Apple's Human Interface Guidelines
- 🔐 **Secure Authentication** - Email/Password and Google Sign-In support
- 📊 **Smart Analytics** - Visual charts and detailed expense analysis
- 📄 **PDF Reports** - Generate comprehensive expense reports
- 🍽️ **Meal Tracking** - Specialized tracking for bachelor mess and trip meals
- ⚡ **Real-time Sync** - Powered by Firebase for instant updates across devices

---

## ✨ Features

### 🔐 Authentication
- Email/Password authentication
- Google Sign-In integration
- Secure user profile management

### 👥 Group Management
- Create groups (Trip or Bachelor Mess)
- Invite members via email
- Group details and member management
- Close groups and generate final reports

### 💸 Expense Management
- **Multiple Split Types:**
  - Equal split
  - Unequal split (custom amounts)
  - Share-based split
- Receipt photo upload
- Expense history and details
- Real-time expense tracking

### 📊 Analytics & Settlement
- **Dashboard Analytics:**
  - Total expenses and amounts
  - Spending trends and patterns
  - Member balance tracking
- **Settlement Calculation:**
  - Automatic "Who owes Whom" calculation
  - Optimized settlement transactions
  - Visual balance indicators
- **Detailed Reports:**
  - Comprehensive PDF generation
  - Expense breakdowns
  - Member contribution analysis

### 🍽️ Meal Tracking
- **Bachelor Mess Tracking:**
  - Monthly market expense calculation
  - Meal count per person
  - Cost per meal calculation
  - Individual balance tracking
- **Trip Meal Tracking:**
  - Outside meal expense tracking
  - Monthly expense distribution
  - Per-meal cost calculation

### 📄 PDF Generation
- Complete expense reports
- Settlement summaries
- Detailed expense breakdowns
- Shareable PDF documents

---

## 🖼️ Screenshots

<div align="center">

### Authentication & Dashboard
| Login Screen | Dashboard | Groups List |
|:---:|:---:|:---:|
| *Login with Email/Google* | *Personal Dashboard* | *All Your Groups* |

### Group Management
| Create Group | Group Details | Add Expense |
|:---:|:---:|:---:|
| *Create New Groups* | *View Group Info* | *Add Expenses* |

### Analytics & Reports
| Settlement Screen | Analytics | PDF Report |
|:---:|:---:|:---:|
| *Who Owes Whom* | *Expense Analytics* | *Generated PDF* |

### Meal Tracking
| Mess Meals | Outside Meals | Meal Statistics |
|:---:|:---:|:---:|
| *Bachelor Mess Tracking* | *Trip Meal Tracking* | *Monthly Calculations* |

</div>

> 📸 *Screenshots coming soon - Add your app screenshots here!*

---

## 🚀 Installation

### Quick Start

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd Split/split
   ```

2. **Install dependencies:**
   ```bash
   flutter pub get
   ```

3. **Set up Firebase** (see detailed guide below)

4. **Run the app:**
   ```bash
   flutter run
   ```

### 📚 Complete Setup Guide

**For a comprehensive step-by-step setup process including Firebase configuration, database setup, and troubleshooting, please see:**

👉 **[SETUP_GUIDE.md](SETUP_GUIDE.md)** - Complete setup instructions

The setup guide includes:
- ✅ Prerequisites and software installation
- ✅ Firebase project creation and configuration
- ✅ Authentication setup (Email/Password + Google Sign-In)
- ✅ Firestore database setup with security rules
- ✅ Firebase Storage configuration
- ✅ Android and iOS app registration
- ✅ SHA-1 fingerprint setup for Google Sign-In
- ✅ Configuration file placement
- ✅ Database structure and indexes
- ✅ Troubleshooting common issues

### Quick Firebase Setup Checklist

- [ ] Create Firebase project
- [ ] Enable Authentication (Email/Password + Google)
- [ ] Create Firestore database with security rules
- [ ] Enable Storage with security rules
- [ ] Register Android app and download `google-services.json`
- [ ] Add SHA-1 fingerprint for Google Sign-In
- [ ] Place `google-services.json` in `android/app/`
- [ ] Configure `firebase_options.dart` (or run `flutterfire configure`)

For detailed instructions, see [SETUP_GUIDE.md](SETUP_GUIDE.md)

For TestFlight distribution guide, see [TESTFLIGHT_GUIDE.md](TESTFLIGHT_GUIDE.md)

---

## 📖 Usage

### Getting Started

1. **Sign Up / Login:**
   - Create an account with email/password or use Google Sign-In
   - Complete your profile

2. **Create a Group:**
   - Tap the "Groups" tab
   - Click "Create Group"
   - Choose group type (Trip or Bachelor Mess)
   - Add group name and description
   - Invite members by email

3. **Add Expenses:**
   - Open a group
   - Tap the "+" button
   - Enter expense details:
     - Amount and description
     - Who paid
     - Split type (Equal/Unequal/Shares)
     - Optional receipt photo
   - Save the expense

4. **Track Meals (Bachelor Mess):**
   - Open a Bachelor Mess group
   - Tap "Mess Meals"
   - Select month
   - Add meals (Breakfast/Lunch/Dinner)
   - View monthly calculations and balances

5. **View Analytics:**
   - Open any group
   - Tap "Analytics" button
   - View detailed expense analysis
   - Check member balances
   - See settlement calculations

6. **Generate PDF Report:**
   - Open a group
   - Tap "Close Group & Generate PDF"
   - Confirm and wait for PDF generation
   - Share or print the report

---

## 🛠️ Tech Stack

### Frontend
- **Flutter** - Cross-platform UI framework
- **Dart** - Programming language
- **Cupertino Design** - iOS-style UI components

### Backend & Services
- **Firebase Authentication** - User authentication
- **Cloud Firestore** - Real-time database
- **Firebase Storage** - Receipt image storage
- **Google Sign-In** - Social authentication

### State Management
- **Provider** - State management solution

### Navigation
- **GoRouter** - Declarative routing

### Additional Packages
- `image_picker` - Receipt photo capture
- `fl_chart` - Data visualization
- `pdf` & `printing` - PDF generation
- `intl` - Date/number formatting
- `uuid` - Unique ID generation
- `equatable` - Value equality

---

## 📁 Project Structure

```
split/
├── lib/
│   ├── main.dart                 # App entry point
│   ├── firebase_options.dart     # Firebase configuration
│   │
│   ├── models/                   # Data models
│   │   ├── user_model.dart
│   │   ├── group_model.dart
│   │   ├── expense_model.dart
│   │   └── meal_model.dart
│   │
│   ├── services/                 # Business logic
│   │   ├── auth_service.dart
│   │   ├── user_service.dart
│   │   ├── group_service.dart
│   │   ├── expense_service.dart
│   │   ├── meal_service.dart
│   │   ├── settlement_service.dart
│   │   └── pdf_service.dart
│   │
│   ├── screens/                   # UI screens
│   │   ├── auth/
│   │   │   ├── login_screen.dart
│   │   │   └── signup_screen.dart
│   │   ├── dashboard/
│   │   │   └── dashboard_screen.dart
│   │   ├── groups/
│   │   │   ├── groups_list_screen.dart
│   │   │   ├── create_group_screen.dart
│   │   │   └── group_details_screen.dart
│   │   ├── expenses/
│   │   │   ├── add_expense_screen.dart
│   │   │   ├── settlement_screen.dart
│   │   │   └── analytics_screen.dart
│   │   ├── meals/
│   │   │   ├── meal_tracking_screen.dart
│   │   │   └── outside_meal_screen.dart
│   │   └── profile/
│   │       └── profile_screen.dart
│   │
│   ├── utils/                     # Utilities
│   │   └── router.dart            # Navigation routes
│   │
│   └── widgets/                   # Reusable widgets
│       └── bottom_nav_shell.dart
│
├── android/                       # Android configuration
├── ios/                           # iOS configuration
├── pubspec.yaml                   # Dependencies
└── README.md                      # This file
```

---

## 🎯 Key Features Explained

### Expense Splitting Algorithms

**Equal Split:**
- Automatically divides expense equally among all members

**Unequal Split:**
- Allows custom amounts for each member
- Validates total equals expense amount

**Share-based Split:**
- Distributes expense based on shares (e.g., 2:1:1)
- Calculates proportional amounts automatically

### Settlement Calculation

The app uses an optimized algorithm to minimize transactions:
1. Calculates net balance for each member
2. Identifies debtors (negative balance) and creditors (positive balance)
3. Matches debts with credits efficiently
4. Generates minimal settlement transactions

### Meal Tracking System

**Monthly Calculation:**
- Filters market/grocery expenses by month
- Counts total meals eaten in the month
- Calculates: `Cost Per Meal = Total Market Expense / Total Meals`
- Tracks individual meal counts and balances

---

## 🔧 Configuration

### Firebase Setup

1. Create Firebase project
2. Enable Authentication methods
3. Create Firestore database
4. Set up Storage bucket
5. Add configuration files to project

### Package Configuration

Update `pubspec.yaml` if you need to modify dependencies or app version.

### App Information

- **Package Name:** `com.splitter.split`
- **App Name:** Splitter
- **Version:** 1.0.0+1

---

## 🧪 Testing

```bash
# Run tests
flutter test

# Run with coverage
flutter test --coverage
```

---

## 📝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Code Style

- Follow Dart/Flutter style guidelines
- Use meaningful variable and function names
- Add comments for complex logic
- Maintain Cupertino design consistency

---

## 🐛 Known Issues

- [ ] iOS requires additional Firebase configuration
- [ ] Some Firestore queries may need composite indexes
- [ ] PDF generation requires proper permissions

---

## 🔮 Future Enhancements

- [ ] Multi-currency support
- [ ] Recurring expenses
- [ ] Expense categories and budgets
- [ ] Export to CSV/Excel
- [ ] Dark mode support
- [ ] Push notifications
- [ ] Expense reminders
- [ ] Group chat feature

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Your Name**
- GitHub: [@yourusername](https://github.com/yourusername)
- Email: email@example.com

---

## 🙏 Acknowledgments

- Flutter team for the amazing framework
- Firebase for backend services
- Cupertino design system
- All contributors and testers

---

## 📞 Support

If you encounter any issues or have questions:

1. Check [SETUP_GUIDE.md](SETUP_GUIDE.md) for setup help
2. Check [TESTFLIGHT_GUIDE.md](TESTFLIGHT_GUIDE.md) for iOS distribution
3. Open an issue on GitHub
4. Check existing issues for solutions

---
