# 📱 Day 01: Setup Expo & Running Your First App on Your Phone

Welcome to **Day 1 of Mobile App Development**! Today, you are going to write code on your computer, scan a QR code with your phone, and watch your mobile app run live on your physical device.

---

## 💡 What is React Native & Expo?

- **React Native**: A framework created by Meta (Facebook) that allows you to write mobile apps in JavaScript. Unlike normal web pages, it renders **real native Android and iOS components**.
- **Expo**: A tool that makes React Native 100x easier. Without Expo, you would need to download 30 Gigabytes of Android Studio, configure Java SDKs, and wait 10 minutes to compile. With Expo, you run one command and test immediately on your phone.

---

## 🛠️ Step-by-Step Setup Guide (Do This Once)

### Step 1: Install Node.js
If you don't have Node.js yet:
1. Go to [nodejs.org](https://nodejs.org/).
2. Download the version that says **LTS (Recommended for Most Users)**.
3. Install it (just click Next, Next, Finish).

### Step 2: Install Expo Go on Your Physical Mobile Phone
1. Take your phone.
2. Open **Google Play Store** (Android) or **Apple App Store** (iPhone).
3. Search for: **Expo Go** (It has a black and white triangle icon).
4. Tap **Install**.

---

## 💻 Building Your First Mobile Project

Now, let's create the project on your computer!

### Step 1: Open Terminal / Command Prompt
Open your terminal or command prompt in your working folder and run:

```bash
npx create-expo-app MyFirstMobileApp
```

Wait about 1 to 2 minutes while it downloads all the starter files.

### Step 2: Enter the Project Folder
```bash
cd MyFirstMobileApp
```

### Step 3: Start the Development Server
```bash
npx expo start
```

You will see a large **QR code** appear right in your terminal window!

---

## 📱 Viewing the App on Your Phone!

1. Make sure your computer and your phone are connected to the **same Wi-Fi network**.
2. **On Android**: Open the **Expo Go** app on your phone -> Tap **"Scan QR code"** -> Point your camera at the QR code on your computer screen.
3. **On iPhone**: Open the normal Camera app -> Point at the QR code -> Tap the yellow notification that says *"Open in Expo Go"*.

🎉 **Boom!** Your phone will load for a few seconds, and you will see your first mobile screen: *"Open up App.js to start working on your app!"*

---

## 🔍 Understanding the Code: What is in `App.js`?

Open `MyFirstMobileApp` inside VS Code and open `App.js`. You will see:

```javascript
import { StatusBar } from 'expo-status-bar';
import { StyleSheet, Text, View } from 'react-native';

export default function App() {
  return (
    <View style={styles.container}>
      <Text>Open up App.js to start working on your app!</Text>
      <StatusBar style="auto" />
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#fff',
    alignItems: 'center',
    justifyContent: 'center',
  },
});
```

### 📖 Line-by-Line Breakdown:
1. `import { Text, View } from 'react-native';`:
   - In websites, we use `<div>` and `<p>`.
   - In Mobile Apps, **`<div>` does NOT exist!** We use **`<View>`** instead (a container/box).
   - In Mobile Apps, raw text is **NOT allowed** outside a tag. You **must** wrap all words inside **`<Text>`**.
2. `export default function App() { ... }`: This is your main mobile screen. Whatever you return here is drawn on your phone screen.
3. `<StatusBar style="auto" />`: Controls the battery, Wi-Fi, and time icons at the very top of your phone.
4. `const styles = StyleSheet.create({ ... })`: Where we style our app (colors, centering, sizes).

---

## 🎯 Day 01 Hands-On Challenge

Now change the code in `App.js` to build your own custom welcome screen:

### Your Task:
1. Change the text to say:
   - Line 1: **"Hello World! My name is [Your Name]"**
   - Line 2: **"I am learning Mobile App Development!"**
2. Change the background color of the phone screen from white (`#fff`) to a cool dark navy blue (`#0f172a`).
3. Make the text color white (`#ffffff`) and make the font size bigger so it looks like a headline!

### 💡 Solution Code:
Replace everything in `App.js` with this:

```javascript
import { StatusBar } from 'expo-status-bar';
import { StyleSheet, Text, View } from 'react-native';

export default function App() {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>Hello World! My name is Delwin 👋</Text>
      <Text style={styles.subtitle}>I am learning Mobile App Development!</Text>
      <StatusBar style="light" />
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#0f172a', // Dark navy background
    alignItems: 'center',
    justifyContent: 'center',
    padding: 20,
  },
  title: {
    fontSize: 24,
    fontWeight: 'bold',
    color: '#ffffff',
    textAlign: 'center',
    marginBottom: 10,
  },
  subtitle: {
    fontSize: 16,
    color: '#94a3b8',
    textAlign: 'center',
  },
});
```

Press **`Ctrl + S`** in VS Code to save.
Look at your phone—it will **automatically refresh instantly** without pressing any button! That is the magic of React Native Fast Refresh!

---

## ✅ Day 01 Check-off
1. [ ] Successfully launched Expo development server.
2. [ ] Scanned QR code and opened app on a real phone.
3. [ ] Customized `App.js` with your own name and dark theme background.
4. [ ] Mark Day 1 as completed in your `TRACKER.md`!
