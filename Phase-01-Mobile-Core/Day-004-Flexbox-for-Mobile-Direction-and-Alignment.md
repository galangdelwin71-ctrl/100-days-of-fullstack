# 📱 Day 04: Mobile Layouts with Flexbox

In web development, elements stack left-to-right (`row`) by default.
In **Mobile Development (React Native)**, elements stack **top-to-bottom (`column`) by default** because phones are vertical screens!

Today, you will master the 3 Flexbox rules that dictate all mobile layouts.

---

## 📐 1. The 3 Golden Flexbox Rules of Mobile

### Rule 1: `flexDirection`
- `column` (Default): Items stack vertically (one under another).
- `row`: Items sit side-by-side horizontally (like a row of buttons or icons).

### Rule 2: `justifyContent` (Main Axis)
Aligns items along the direction of flow:
- `flex-start`: Placed at the top (or left if row).
- `center`: Centered in the middle.
- `flex-end`: Placed at the bottom (or right if row).
- `space-between`: Pushed to the extreme opposite ends (e.g., Logo on the left, Cart icon on the far right!).
- `space-around`: Equal spacing around each item.

### Rule 3: `alignItems` (Cross Axis)
Aligns items perpendicular to the main axis:
- `center`: Centers items across the screen.
- `flex-start` / `flex-end`.
- `stretch`: Stretches items to fill full width.

---

## 💻 Step-by-Step Code: Mobile App Header with Flexbox Row

Look at how top apps align their header:
- Left: Profile Avatar
- Middle: Welcome text
- Right: Notification Bell

Replace `App.js` with this code:

```javascript
import { StatusBar } from 'expo-status-bar';
import { StyleSheet, Text, View, Image } from 'react-native';

export default function App() {
  return (
    <View style={styles.screen}>
      
      {/* TOP HEADER BAR */}
      <View style={styles.headerBar}>
        
        {/* Left Side: Avatar + Greeting (Row) */}
        <View style={styles.userSection}>
          <Image 
            source={{ uri: 'https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?w=120' }}
            style={styles.avatar}
          />
          <View>
            <Text style={styles.welcomeText}>Welcome back,</Text>
            <Text style={styles.userName}>Delwin Galang</Text>
          </View>
        </View>

        {/* Right Side: Notification Icon Badge */}
        <View style={styles.bellBadge}>
          <Text style={styles.bellIcon}>🔔</Text>
        </View>

      </View>

      {/* STATS SECTION (3 Columns in a Row) */}
      <View style={styles.statsRow}>
        <View style={styles.statBox}>
          <Text style={styles.statNumber}>12</Text>
          <Text style={styles.statLabel}>Tasks</Text>
        </View>
        <View style={styles.statBox}>
          <Text style={styles.statNumber}>85%</Text>
          <Text style={styles.statLabel}>Done</Text>
        </View>
        <View style={styles.statBox}>
          <Text style={styles.statNumber}>4.9</Text>
          <Text style={styles.statLabel}>Rating</Text>
        </View>
      </View>

      <StatusBar style="light" />
    </View>
  );
}

const styles = StyleSheet.create({
  screen: {
    flex: 1,
    backgroundColor: '#0b0f19',
    paddingTop: 60, // Space for phone notch/status bar
    paddingHorizontal: 20,
  },
  headerBar: {
    flexDirection: 'row', // Horizontal placement
    justifyContent: 'space-between', // Pushes user info to left and bell to right
    alignItems: 'center',
    paddingBottom: 24,
    borderBottomWidth: 1,
    borderBottomColor: '#1e293b',
  },
  userSection: {
    flexDirection: 'row',
    alignItems: 'center',
    gap: 12,
  },
  avatar: {
    width: 48,
    height: 48,
    borderRadius: 24,
  },
  welcomeText: {
    fontSize: 12,
    color: '#94a3b8',
  },
  userName: {
    fontSize: 16,
    fontWeight: 'bold',
    color: '#ffffff',
  },
  bellBadge: {
    width: 44,
    height: 44,
    borderRadius: 22,
    backgroundColor: '#1e293b',
    alignItems: 'center',
    justifyContent: 'center',
  },
  bellIcon: {
    fontSize: 18,
  },
  statsRow: {
    flexDirection: 'row', // 3 cards in a horizontal row
    justifyContent: 'space-between',
    marginTop: 24,
    gap: 12,
  },
  statBox: {
    flex: 1, // Each card takes equal 1/3 share of width!
    backgroundColor: '#1e293b',
    padding: 16,
    borderRadius: 16,
    alignItems: 'center',
  },
  statNumber: {
    fontSize: 22,
    fontWeight: 'bold',
    color: '#38bdf8',
  },
  statLabel: {
    fontSize: 12,
    color: '#94a3b8',
    marginTop: 4,
  },
});
```

---

## 🎯 Day 04 Daily Challenge

Build an **"Action Row"** underneath the stats with 2 buttons side-by-side using `flexDirection: 'row'`!
- Button 1: `"Deposit Cash"` (takes `flex: 1`, green background).
- Button 2: `"Send Money"` (takes `flex: 1`, blue background).
- Test it on your phone!
