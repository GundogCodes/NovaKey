# HyperKey

<div align="center">
  <img src="https://img.shields.io/badge/Platform-macOS-blue.svg" alt="Platform: macOS">
  <img src="https://img.shields.io/badge/Available-Mac_App_Store-black.svg" alt="Available on Mac App Store">
  <img src="https://img.shields.io/badge/Language-Swift-orange.svg" alt="Language: Swift">
  <img src="https://img.shields.io/badge/Framework-SwiftUI-green.svg" alt="Framework: SwiftUI">
</div>

A sleek, modern macOS application launcher that lets you instantly open any app with custom keyboard shortcuts. Built with SwiftUI and designed for productivity enthusiasts who want lightning-fast access to their favorite applications.

**Available now on the Mac App Store!**

## ✨ Features

### 🚀 **Lightning Fast App Launching**
- Set custom keyboard shortcuts for any application
- Instant app launching without dock or Spotlight delays
- Support for complex modifier key combinations (⌃⌥⇧⌘)

### 🔍 **Smart Search & Organization**
- Real-time search and filtering of configured hotkeys
- Search by app name, shortcut combination, or hotkey name
- Clean, organized interface showing all your shortcuts at a glance

### 📊 **Usage Analytics**
- Track how often you use each hotkey
- View detailed usage statistics and patterns
- Identify your most and least used shortcuts
- See when you last used each hotkey

### 🎨 **Beautiful Interface**
- Native macOS dark mode design
- Futuristic neon-glow HyperKey branding
- Smooth animations and hover effects
- Real app icons displayed for each shortcut

### ⚙️ **System Integration**
- Launch at login support
- Menu bar integration for easy access
- Helpful macOS window management tips
- Respects system accessibility settings

## 📱 Screenshots

<div align="center">
  <img width="540" height="310" alt="HyperKey Main Interface" src="https://github.com/user-attachments/assets/905aee00-ea27-47c5-b7c6-e4ea31b71299" />
  <img width="540" height="310" alt="HyperKey Settings" src="https://github.com/user-attachments/assets/e5753785-bbc8-4527-a629-3636e1c29330" />
</div>

<div align="center">
  <img width="540" height="310" alt="HyperKey Usage Statistics" src="https://github.com/user-attachments/assets/ba013908-93b3-4828-b665-51936d20c7be" />
</div>

## 🛒 Download

### Mac App Store
[**Download HyperKey from the Mac App Store**](https://apps.apple.com/ca/app/hyperkey/id6751394828?mt=12)

### System Requirements
- macOS 12.0 (Monterey) or later
- Accessibility permissions for global hotkey registration

## 🚀 Quick Start

1. **Download from Mac App Store** - Search for "HyperKey" or use the link above
2. **Grant Permissions** - Allow accessibility access when prompted
3. **Launch HyperKey** - The app runs in the background with a menu bar icon
4. **Open Preferences** - Click the menu bar icon and select "HyperKey Preferences"
5. **Add Your First Hotkey**:
   - Click the `+` button
   - Enter a name (e.g., "Launch Safari")
   - Choose your keyboard shortcut (e.g., `⌃⌥S`)
   - Select the target application
   - Click "Add Hotkey"
6. **Test It Out** - Press your keyboard shortcut to launch the app instantly!

## ⌨️ Usage Examples

### Common Hotkey Patterns

| Shortcut | App | Description |
|----------|-----|-------------|
| `⌃⌥C` | Chrome/Safari | Quick web browsing |
| `⌃⌥T` | Terminal | Instant terminal access |
| `⌃⌥V` | VS Code | Jump to coding |
| `⌃⌥S` | Slack/Discord | Communication apps |
| `⌃⌥M` | Music/Spotify | Media control |
| `⌃⌥N` | Notes | Quick note-taking |

### Pro Tips

- **Use consistent patterns**: Group similar apps with similar modifier combinations
- **Avoid system shortcuts**: Check that your shortcuts don't conflict with macOS defaults
- **Start simple**: Begin with your most-used apps, then expand
- **Check statistics**: Use the built-in analytics to optimize your shortcuts

## 🔧 Configuration

### Window Management Issues?

If apps are resizing existing windows when launched, disable these macOS features:

1. **System Settings → Desktop & Dock → Mission Control**
2. Turn off:
   - ✅ Stage Manager
   - ✅ "Automatically rearrange Spaces"
   - ✅ "Switch to app's Space when activated"

### Launch at Login

Enable "Launch at Login" in HyperKey preferences to have your shortcuts ready immediately after boot.

### Accessibility Permissions

HyperKey requires accessibility permissions to register global hotkeys:

1. **System Settings → Privacy & Security → Accessibility**
2. Click the `+` button and add HyperKey
3. Toggle the switch to enable permissions
4. Restart HyperKey if needed

## 📋 Version History

### Latest Release
- ✨ Smart search and filtering
- 🎨 Real app icon display
- 📊 Usage statistics and analytics
- 🐛 Bug fixes and performance improvements

*See App Store for complete version history*

## ❓ Frequently Asked Questions

### **Q: Why does HyperKey need accessibility permissions?**
A: HyperKey needs accessibility permissions to register system-wide keyboard shortcuts. This is a macOS requirement for any app that listens for global hotkeys.

### **Q: Can I use the same shortcut for multiple apps?**
A: No, each keyboard shortcut must be unique. HyperKey will warn you if you try to create a duplicate shortcut.

### **Q: Does HyperKey work with all apps?**
A: Yes! HyperKey can launch any application installed on your Mac, including apps from the App Store, third-party apps, and system utilities.

### **Q: Will my shortcuts work after restarting my Mac?**
A: Yes, if you enable "Launch at Login" in HyperKey preferences, all your shortcuts will be available immediately after startup.

### **Q: Can I backup my hotkey configurations?**
A: Your hotkey configurations are automatically saved and will persist across app updates. For manual backup, you can export your settings (feature coming in future update).

## 🏗 Technical Details

### Technologies Used
- **SwiftUI**: Modern declarative UI framework
- **Carbon Framework**: Low-level hotkey registration
- **AppKit**: macOS-specific functionality
- **NSWorkspace**: Application launching and management

### Privacy & Security
- All data is stored locally on your Mac
- No network connections or data collection
- No encryption algorithms implemented
- Uses standard macOS data protection
- [Privacy Policy](https://gundogcodes.github.io/hyperkey-privacy-policy/)

## 💬 Support & Feedback

### 📧 Contact
- **App Store Reviews**: Leave feedback directly on the Mac App Store
- **Support Email**: gunishsharma20@gmail.com
- **Feature Requests**: Contact via email with your suggestions

### 🐛 Reporting Issues
When reporting issues, please include:
- macOS version
- HyperKey version (from App Store)
- Steps to reproduce the issue
- Screenshots if applicable

## 🔄 Updates

HyperKey is actively maintained with regular updates including:
- New features based on user feedback
- Performance improvements
- macOS compatibility updates
- Bug fixes and stability enhancements

Updates are delivered automatically through the Mac App Store.

## 🏆 Reviews & Recognition

*"HyperKey has revolutionized how I work on my Mac. Lightning-fast app switching!"*

*"Clean interface, reliable performance, and great statistics tracking."*

*"Finally, a hotkey manager that just works and looks beautiful doing it."*

⭐⭐⭐⭐⭐ **Leave a review on the Mac App Store to support development!**

---

<div align="center">
  <p><strong>🚀 <a href="https://apps.apple.com/ca/app/hyperkey/id6751394828?mt=12">Download HyperKey from the Mac App Store</a></strong></p>
  <p>Made with ❤️ for the macOS community</p>
</div>
