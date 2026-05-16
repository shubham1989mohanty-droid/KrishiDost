# KrishiDost 🌾

**A platform to help Indian farmers on max possible ways**

## 📱 About

KrishiDost is an Android application designed to provide comprehensive support and guidance to Indian farmers through technology. The app aims to help farmers with various aspects of modern farming practices.

## 🚀 Quick Start

### Prerequisites
- **JDK 17** (Required) - [Installation Guide](./JDK17_FIX_GUIDE.md)
- Android Studio (latest version)
- Git
- Gradle 8.0+

### Setup
```bash
git clone https://github.com/shubham1989mohanty-droid/KrishiDost.git
cd KrishiDost
```

Detailed setup instructions: [SETUP_INSTRUCTIONS.md](./SETUP_INSTRUCTIONS.md)

### Build
```bash
# Android APK
./gradlew assembleDebug

# Or use Android Studio
# Build → Build Bundle(s)/APK(s) → Build APK(s)
```

---

## 🛠️ Technology Stack

| Technology | Version | Purpose |
|-----------|---------|---------|
| **Language** | Dart | Primary development language |
| **JDK** | 17 | Build system requirement |
| **Gradle** | 8.0+ | Build automation |
| **Android SDK** | 34 | Target Android version |
| **Min SDK** | 21 | Minimum Android version |

---

## 📂 Project Structure

```
KrishiDost/
├── lib/                      # Source code
├── android/                  # Android-specific configuration
├── build.gradle              # Project build configuration
├── gradle.properties         # Gradle settings
├── SETUP_INSTRUCTIONS.md     # Complete setup guide
├── JDK17_FIX_GUIDE.md        # JDK 17 configuration troubleshooting
└── README.md                 # This file
```

---

## 📋 Build Configuration

- **Compile SDK**: 34
- **Target SDK**: 34
- **Min SDK**: 21
- **JDK**: 17.0.x (Required)
- **Gradle**: 8.0.0+
- **Kotlin**: 1.8.0+
- **Build Tools**: 34.0.0

---

## 🐛 Common Issues & Solutions

### JDK 17 Configuration Issue
If you encounter JDK 17-related build errors:
→ See [JDK17_FIX_GUIDE.md](./JDK17_FIX_GUIDE.md)

### Build Sync Failed
1. File → Invalidate Caches → Invalidate and Restart
2. Delete `.gradle` folder in home directory
3. Try sync again

### Gradle Not Found
Ensure `JAVA_HOME` is correctly set to JDK 17:
```bash
java -version  # Should show 17.x.x
```

---

## 📖 Documentation

- **[Setup Instructions](./SETUP_INSTRUCTIONS.md)** - Complete guide to set up the project
- **[JDK 17 Fix Guide](./JDK17_FIX_GUIDE.md)** - Troubleshooting JDK and Gradle issues
- **[GitHub Issues](https://github.com/shubham1989mohanty-droid/KrishiDost/issues)** - Report bugs and request features

---

## 🔧 Build Commands

```bash
# Build debug APK
./gradlew assembleDebug

# Build release APK
./gradlew assembleRelease

# Install on device
./gradlew installDebug

# Run tests
./gradlew test

# Clean build
./gradlew clean build

# View version info
./gradlew --version
```

---

## 🤝 Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add YourFeature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

---

## 📄 License

This project is open source and available under the MIT License.

---

## 👤 Author

**shubham1989mohanty-droid**
- GitHub: [@shubham1989mohanty-droid](https://github.com/shubham1989mohanty-droid)

---

## 📞 Support

For issues or questions:
- Check [SETUP_INSTRUCTIONS.md](./SETUP_INSTRUCTIONS.md)
- Review [JDK17_FIX_GUIDE.md](./JDK17_FIX_GUIDE.md)
- Open an [issue on GitHub](https://github.com/shubham1989mohanty-droid/KrishiDost/issues)

---

## ✅ Status

- ✅ Project initialized
- ✅ JDK 17 build configuration
- ✅ Gradle setup optimized
- ✅ Documentation complete
- 🔄 Development in progress

---

**Last Updated**: 2026-05-16  
**Current Version**: Initial Setup  
**Maintainer**: shubham1989mohanty-droid
