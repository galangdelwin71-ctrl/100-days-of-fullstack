# 📱 Day 02: Core UI Components — View, Text & Image

On Day 1, you learned that web tags like `<div>`, `<p>`, and `<img>` do not exist in native mobile development. Today, you will master the 3 core building blocks that make up 90% of every screen in Instagram, TikTok, and Twitter: **View**, **Text**, and **Image**.

---

## 🧱 1. The 3 Core Building Blocks

### A. `<View>` — The Universal Mobile Box
- Think of `<View>` as a box or container.
- It is used to group things together, create cards, banners, or full-screen wrappers.
- It uses **Flexbox by default** (everything inside stacks vertically from top to bottom).

### B. `<Text>` — Rendering Typography
- In mobile development, you **cannot** write text directly inside a `<View>`.
- ❌ **Wrong (Will Crash App)**: `<View>Hello</View>`
- ✅ **Correct**: `<View><Text>Hello</Text></View>`
- `<Text>` supports nesting:
  ```javascript
  <Text>
    Welcome to <Text style={{ fontWeight: 'bold', color: '#38bdf8' }}>FordaGo</Text>!
  </Text>
  ```

### C. `<Image>` — Displaying Photos & Graphics
Mobile images come in two types:
1. **Network Images (From the Internet)**:
   - Must provide a URL and **must explicitly define `width` and `height`**, otherwise React Native will not know how large it is and will show a blank screen!
   ```javascript
   <Image 
     source={{ uri: 'https://images.unsplash.com/photo-1535713875002-d1d0cf377fde' }}
     style={{ width: 100, height: 100, borderRadius: 50 }}
   />
   ```
2. **Local Images (Stored in your project folder)**:
   - Uses `require('./path/to/image.png')`.

---

## 💻 Step-by-Step Code Example: Building an Avatar Card

Let's build a real User Avatar Profile Card.

Replace your `App.js` with:

```javascript
import { StatusBar } from 'expo-status-bar';
import { StyleSheet, Text, View, Image } from 'react-native';

export default function App() {
  return (
    <View style={styles.screen}>
      
      {/* Profile Card Container */}
      <View style={styles.card}>
        {/* Profile Picture */}
        <Image 
          source={{ uri: 'https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=400' }}
          style={styles.avatar}
        />

        {/* User Details */}
        <Text style={styles.name}>Maria Santos</Text>
        <Text style={styles.role}>Mobile Software Engineer</Text>
        <Text style={styles.bio}>
          Building cross-platform mobile apps with React Native & Expo. 🚀
        </Text>
      </View>

      <StatusBar style="light" />
    </View>
  );
}

const styles = StyleSheet.create({
  screen: {
    flex: 1,
    backgroundColor: '#0f172a', // Dark slate background
    alignItems: 'center',
    justifyContent: 'center',
    padding: 20,
  },
  card: {
    backgroundColor: '#1e293b', // Lighter slate card box
    borderRadius: 20,
    padding: 24,
    alignItems: 'center',
    width: '100%',
    maxWidth: 320,
    borderWidth: 1,
    borderColor: '#334155',
  },
  avatar: {
    width: 100,
    height: 100,
    borderRadius: 50, // Makes it a perfect circle!
    marginBottom: 16,
    borderWidth: 3,
    borderColor: '#38bdf8', // Cyan border
  },
  name: {
    fontSize: 22,
    fontWeight: 'bold',
    color: '#f8fafc',
    marginBottom: 4,
  },
  role: {
    fontSize: 14,
    fontWeight: '600',
    color: '#38bdf8',
    marginBottom: 12,
  },
  bio: {
    fontSize: 14,
    color: '#94a3b8',
    textAlign: 'center',
    lineHeight: 20,
  },
});
```

---

## 🎯 Day 02 Daily Challenge

Modify the code above to create a **"Product Showcase Card"** (like a shopping item in Shopee or Lazada):

### Requirements:
1. Replace the person image with a product picture (e.g. sneakers, headphones, or food).
   - Tip: You can use this free Unsplash image URL: `https://images.unsplash.com/photo-1505740420928-5e560c06d30e?w=500` (Headphones).
2. Change the dimensions of the `<Image>` so it is a rectangle (`width: '100%'`, `height: 180`, `borderRadius: 12`).
3. Add:
   - Product Name (e.g., **"Wireless Noise-Cancelling Headphones"**) in bold.
   - Price text (e.g., **"₱2,499.00"**) in bright green (`#22c55e`).
   - Short description text below the price.

Save the file, check your phone, and see your product card live!
