# 📱 Day 03: Mobile Styling with StyleSheet & Colors

In web development, you write CSS files with classes like `.my-button`. In React Native, styling is written in pure JavaScript using **`StyleSheet.create()`**. Today, you will master mobile design tokens, padding, borders, shadows, and color theory.

---

## 🎨 1. How Styling Works in React Native

Instead of kebab-case like `background-color` or `font-size`, React Native uses **camelCase**:
- `background-color` ➔ `backgroundColor`
- `font-size` ➔ `fontSize`
- `margin-top` ➔ `marginTop`
- `border-radius` ➔ `borderRadius`

### Notice: No "px" units!
In CSS you write `padding: 20px;`. In React Native, **you do not write "px"**! You just write plain numbers:
- `padding: 20`
- `fontSize: 18`
- `width: 250`
React Native automatically scales these numbers to match the exact pixel density (DPI) of every phone (iPhone Retina, Samsung AMOLED, budget phones).

---

## 🧱 2. Anatomy of `StyleSheet.create()`

```javascript
import { StyleSheet, View, Text } from 'react-native';

const styles = StyleSheet.create({
  card: {
    backgroundColor: '#ffffff',
    padding: 16,
    borderRadius: 12,
    marginVertical: 10,
  },
  cardTitle: {
    fontSize: 18,
    fontWeight: 'bold',
    color: '#1e293b',
  },
});
```

### Combining Multiple Styles (The Array Syntax)
You can apply multiple style objects to a single component by passing an array:
```javascript
<Text style={[styles.baseText, styles.highlightText]}>Warning!</Text>
```
The style on the right overrides the one on the left.

---

## 💻 Step-by-Step Code: Designing a Modern Status Badge

Replace `App.js` with this code:

```javascript
import { StatusBar } from 'expo-status-bar';
import { StyleSheet, Text, View } from 'react-native';

export default function App() {
  return (
    <View style={styles.screen}>
      <Text style={styles.screenTitle}>Design System Badges</Text>

      {/* Success Badge */}
      <View style={[styles.badge, styles.badgeSuccess]}>
        <Text style={[styles.badgeText, styles.textSuccess]}>● System Online</Text>
      </View>

      {/* Warning Badge */}
      <View style={[styles.badge, styles.badgeWarning]}>
        <Text style={[styles.badgeText, styles.textWarning]}>▲ Low Storage Alert</Text>
      </View>

      {/* Danger Badge */}
      <View style={[styles.badge, styles.badgeDanger]}>
        <Text style={[styles.badgeText, styles.textDanger]}>✖ Payment Failed</Text>
      </View>

      <StatusBar style="light" />
    </View>
  );
}

const styles = StyleSheet.create({
  screen: {
    flex: 1,
    backgroundColor: '#090d16',
    alignItems: 'center',
    justifyContent: 'center',
    padding: 24,
    gap: 16, // Spaces out children automatically!
  },
  screenTitle: {
    fontSize: 22,
    fontWeight: 'bold',
    color: '#ffffff',
    marginBottom: 10,
  },
  badge: {
    paddingVertical: 10,
    paddingHorizontal: 20,
    borderRadius: 30, // Pill shape
    borderWidth: 1,
    width: '80%',
    alignItems: 'center',
  },
  badgeText: {
    fontSize: 14,
    fontWeight: '700',
    letterSpacing: 0.5,
  },
  // Success Variant
  badgeSuccess: {
    backgroundColor: 'rgba(34, 197, 94, 0.15)',
    borderColor: '#22c55e',
  },
  textSuccess: {
    color: '#4ade80',
  },
  // Warning Variant
  badgeWarning: {
    backgroundColor: 'rgba(234, 179, 8, 0.15)',
    borderColor: '#eab308',
  },
  textWarning: {
    color: '#facc15',
  },
  // Danger Variant
  badgeDanger: {
    backgroundColor: 'rgba(239, 68, 68, 0.15)',
    borderColor: '#ef4444',
  },
  textDanger: {
    color: '#f87171',
  },
});
```

---

## 🎯 Day 03 Daily Challenge

Add an **"Info Badge"** and an **"Upgrade Pro Badge"** to the design system above!

### Requirements:
1. **Info Badge**: Sky blue background with blue border (`#0284c7`), saying: `"ℹ New Version Available"`.
2. **Pro VIP Badge**: Purple gradient or violet border (`#a855f7`), saying: `"★ PRO MEMBER"`.
3. Test how it renders on your phone!
