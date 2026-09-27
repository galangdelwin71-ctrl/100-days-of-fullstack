# 📱 Day 05: Touchables & The Pressable Component

On a computer, users click with a mouse. On a mobile phone, users **tap**, **press**, and **hold** with their fingers.

In this lesson, you will learn how to handle touch interactions using React Native's modern **`<Pressable>`** component.

---

## 👆 1. Why `<Pressable>` is Better than Old `<Button>`

React Native has a basic `<Button title="Click Me" />` component, but professional apps **almost never use it** because:
1. You cannot easily style its borders, padding, or icons.
2. It looks completely different and clunky between iOS and Android.

Instead, we use **`<Pressable>`**!
`<Pressable>` allows you to turn ANY View, Text, Card, or Image into a clickable button, complete with touch opacity feedback!

---

## 💻 2. How to Use `<Pressable>` with Press State

`<Pressable>` accepts a style callback function:
```javascript
<Pressable 
  onPress={() => console.log('Tapped!')}
  style={({ pressed }) => [
    styles.button,
    pressed && styles.buttonPressed // Dim or scale when finger touches screen!
  ]}
>
  <Text style={styles.buttonText}>Click Me</Text>
</Pressable>
```

---

## 💻 Step-by-Step Code: Interactive Counter Screen

Replace `App.js` with this code:

```javascript
import { useState } from 'react';
import { StatusBar } from 'expo-status-bar';
import { StyleSheet, Text, View, Pressable, Alert } from 'react-native';

export default function App() {
  const [likes, setLikes] = useState(0);

  const handleLike = () => {
    setLikes(likes + 1);
  };

  const handleReset = () => {
    Alert.alert(
      "Reset Counter",
      "Are you sure you want to reset likes to zero?",
      [
        { text: "Cancel", style: "cancel" },
        { text: "Yes, Reset", onPress: () => setLikes(0), style: "destructive" }
      ]
    );
  };

  return (
    <View style={styles.screen}>
      <Text style={styles.counterText}>{likes}</Text>
      <Text style={styles.subtitleText}>Total Hearts Collected</Text>

      {/* Main Like Button */}
      <Pressable 
        onPress={handleLike}
        style={({ pressed }) => [
          styles.primaryButton,
          pressed && styles.buttonPressed
        ]}
      >
        <Text style={styles.primaryButtonText}>❤️ Give a Like</Text>
      </Pressable>

      {/* Reset Button */}
      <Pressable 
        onPress={handleReset}
        style={({ pressed }) => [
          styles.secondaryButton,
          pressed && styles.buttonPressed
        ]}
      >
        <Text style={styles.secondaryButtonText}>Reset Count</Text>
      </Pressable>

      <StatusBar style="light" />
    </View>
  );
}

const styles = StyleSheet.create({
  screen: {
    flex: 1,
    backgroundColor: '#0f172a',
    alignItems: 'center',
    justifyContent: 'center',
    padding: 24,
  },
  counterText: {
    fontSize: 72,
    fontWeight: '900',
    color: '#f43f5e', // Rose red
  },
  subtitleText: {
    fontSize: 16,
    color: '#94a3b8',
    marginBottom: 40,
  },
  primaryButton: {
    backgroundColor: '#e11d48',
    paddingVertical: 16,
    paddingHorizontal: 36,
    borderRadius: 30,
    width: '100%',
    alignItems: 'center',
    marginBottom: 16,
  },
  primaryButtonText: {
    color: '#ffffff',
    fontSize: 18,
    fontWeight: 'bold',
  },
  secondaryButton: {
    backgroundColor: 'transparent',
    paddingVertical: 14,
    paddingHorizontal: 36,
    borderRadius: 30,
    borderWidth: 1,
    borderColor: '#334155',
    width: '100%',
    alignItems: 'center',
  },
  secondaryButtonText: {
    color: '#94a3b8',
    fontSize: 15,
    fontWeight: '600',
  },
  buttonPressed: {
    opacity: 0.7,
    transform: [{ scale: 0.98 }], // Slightly shrinks on tap like a real physical button!
  },
});
```

---

## 🎯 Day 05 Daily Challenge

Add a third button: **"Subtract (-1)"** button!
- It should decrease the likes count by 1.
- Bonus rule: Do not let the count go below 0 (if `likes === 0`, don't decrease further).
- Tap the buttons on your phone and feel the smooth touch feedback!
