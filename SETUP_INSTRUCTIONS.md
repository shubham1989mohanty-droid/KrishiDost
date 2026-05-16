# KrishiDost Setup Instructions

## 📋 Prerequisites

Before setting up KrishiDost, ensure you have:

1. **Java Development Kit (JDK) 17** ⚠️ **CRITICAL**
   - Download from [Oracle JDK 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html) or use OpenJDK
   - macOS: `brew install openjdk@17`
   - Linux: `sudo apt install openjdk-17-jdk`

2. **Android Studio** (latest version)
   - Download from [Android Studio](https://developer.android.com/studio)

3. **Git** for version control

4. **Gradle** 8.0+ (included with Android Studio)

---

## 🚀 Repository Setup

### Step 1: Clone Repository
```bash
git clone https://github.com/shubham1989mohanty-droid/KrishiDost.git
cd KrishiDost
```

### Step 2: Set JDK 17 Environment Variable

**Windows (Command Prompt - as Administrator):**
```cmd
setx JAVA_HOME "C:\Program Files\Java\jdk-17.0.x"
```

**macOS (Terminal):**
```bash
echo 'export JAVA_HOME=$(/usr/libexec/java_home -v 17)' >> ~/.zshrc
source ~/.zshrc
```

**Linux (Terminal):**
```bash
echo 'export JAVA_HOME=/usr/lib/jvm/java-17-openjdk' >> ~/.bashrc
source ~/.bashrc
```

### Step 3: Verify JDK Installation
```bash
java -version
# Should display: java version "17.x.x"
```

### Step 4: Open in Android Studio
1. Open Android Studio
2. File → Open → Navigate to KrishiDost folder
3. Android Studio will detect and configure the project

### Step 5: Configure Gradle JDK in Android Studio
1. File → Settings → Build, Execution, Deployment → Build Tools → Gradle
2. Set **Gradle JDK** to:
   - **Embedded JDK (17)** OR
   - Browse to your JDK 17 installation
3. Click OK

### Step 6: Sync Project
- Click "Sync Now" when prompted
- Or: File → Sync Now

### Step 7: Build Project
```bash
# Using Gradle wrapper
./gradlew assembleDebug

# Or build through Android Studio
# Build → Build Bundle(s) / APK(s) → Build APK(s)
```

---

## 🔍 Verify Setup Success

Run this command to verify everything is configured correctly:
```bash
./gradlew --version
```

Expected output should show:
- Gradle version 8.0 or higher
- Java version 17.x.x

---

## 📁 Project Structure

```
KrishiDost/
├── build.gradle              # Project-level build configuration (JDK 17)
├── gradle.properties         # Gradle settings with JDK 17 config
├── gradle/
│   └── wrapper/
│       └── gradle-wrapper.properties
├── lib/                      # Dart/Flutter source code
├── android/                  # Android-specific code
├── README.md                 # Project documentation
├── JDK17_FIX_GUIDE.md       # JDK 17 troubleshooting guide
└── SETUP_INSTRUCTIONS.md    # This file
```

---

## ⚙️ Build Configuration Details

### JDK Version
- **Required**: JDK 17
- **Android Gradle Plugin**: 8.0.0+
- **Gradle**: 8.0+
- **Kotlin**: 1.8.0+

### Android Configuration
- **Target SDK**: 34
- **Compile SDK**: 34
- **Min SDK**: 21
- **Build Tools**: 34.0.0

---

## 🛠️ Development Workflow

### Build Debug APK
```bash
./gradlew assembleDebug
# Output: app/build/outputs/apk/debug/app-debug.apk
```

### Install on Device/Emulator
```bash
./gradlew installDebug
```

### Run Tests
```bash
./gradlew test
```

### Clean Build
```bash
./gradlew clean assembleDebug
```

---

## 🐛 Troubleshooting

### Build Error: "Unsupported class-file format"
- **Cause**: Wrong JDK version (not 17)
- **Fix**: [See JDK17_FIX_GUIDE.md](./JDK17_FIX_GUIDE.md)

### Build Error: "Gradle sync failed"
- **Fix 1**: Close Android Studio, delete `.gradle` and `.idea` folders, reopen
- **Fix 2**: Invalidate caches: File → Invalidate Caches → Invalidate and Restart

### Build Error: "JAVA_HOME is not set correctly"
- **Fix**: [Follow JDK Setup Steps](#step-2-set-jdk-17-environment-variable) above

### Port Already in Use
- **Fix**: Kill process on port 8080 or use different port in configuration

---

## 📞 Support

For detailed JDK 17 configuration issues, see: [JDK17_FIX_GUIDE.md](./JDK17_FIX_GUIDE.md)

For general GitHub issues: [KrishiDost Issues](https://github.com/shubham1989mohanty-droid/KrishiDost/issues)

---

## ✅ Checklist Before Development

- [ ] JDK 17 installed and JAVA_HOME set
- [ ] `java -version` shows 17.x.x
- [ ] Android Studio opened KrishiDost project
- [ ] Gradle JDK configured to version 17
- [ ] Project synced successfully (no red errors)
- [ ] `./gradlew --version` runs without errors
- [ ] First build completed: `./gradlew assembleDebug`

---

Happy coding! 🚀
