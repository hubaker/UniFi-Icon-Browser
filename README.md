# UniFi Device Icon Browser

A powerful, client-side tool for browsing and searching UniFi device icons with automatic device name extraction from the UniFi portal.

![UniFi Icon Browser](https://img.shields.io/badge/UniFi-Icon%20Browser-132889?style=for-the-badge&logo=ubiquiti)
![License](https://img.shields.io/badge/license-MIT-blue.svg?style=for-the-badge)
![No Dependencies](https://img.shields.io/badge/dependencies-none-success?style=for-the-badge)

## 🌟 Features

- **🔍 Smart Search** - Search device icons by name or ID across your imported device registry
- **📋 Easy Import** - Extract device names directly from UniFi portal using a bookmarklet
- **💾 Persistent Storage** - Device names are saved locally and persist across sessions
- **🎨 Modern UI** - Beautiful dark mode interface with smooth animations
- **⚡ Fast & Lightweight** - Pure HTML/CSS/JavaScript, no dependencies, no server required
- **📱 Responsive** - Works on desktop and mobile devices
- **🔄 Real-time Updates** - See device count updates as you import

## 🎯 What It Does

This tool solves a common problem for UniFi network administrators: **finding the right device icon quickly**. Instead of scrolling through hundreds of generic icons in the UniFi portal, you can:

1. Extract device names from your UniFi portal
2. Search and browse devices by name
3. Copy device names, IDs, or image URLs with one click
4. Build a personal device registry that grows over time

## 🚀 Quick Start

### Option 1: Direct Use (Recommended)

1. **Download** `unifi-icon-browser.html` to your computer
2. **Open** it in any modern web browser (Chrome, Firefox, Edge, Safari)
3. **Follow** the on-page instructions to set up the bookmarklet
4. **Start browsing** your device icons!

### Option 2: GitHub Pages

1. Fork this repository
2. Enable GitHub Pages in your repository settings
3. Access your instance at `https://yourusername.github.io/unifi-icon-browser/`

## 📖 How to Use

### Step 1: Set Up the Bookmarklet

1. Drag the **"Extract Devices from UniFi Portal"** link to your bookmarks bar
2. Keep this page open in your browser

### Step 2: Extract Device Names

1. Open a **new tab** and navigate to your UniFi portal
2. Log in to your UniFi dashboard
3. Click on any client device
4. Click on the device's icon to open the icon selection modal
5. **While the icon selection modal is open**, click the bookmarklet you created in Step 1
6. You'll see a success message with the number of device IDs extracted
7. The JSON data is automatically copied to your clipboard

### Step 3: Import Device Names

1. Return to the UniFi Icon Browser page
2. Click the **"📋 Paste Import"** button
3. Your device names are now imported and searchable!

### Step 4: Search and Browse

- Type in the search box to filter devices by name or ID
- Click any icon to copy its device name to clipboard
- Use the action buttons to copy device ID or image URL

## 🔧 How It Works

### Architecture

This is a **100% client-side application** - all processing happens in your browser:

- **No backend server** - Everything runs locally
- **No external dependencies** - Pure vanilla JavaScript
- **LocalStorage persistence** - Your data stays on your device
- **Bookmarklet extraction** - Uses React Fiber traversal to extract device data from UniFi portal

### Technical Details

#### Bookmarklet Extraction

The bookmarklet uses advanced techniques to extract device names from the UniFi portal:

1. **React Fiber Traversal** - Traverses React's internal component tree to find device data
2. **DOM Fallback** - Falls back to DOM parsing if React data isn't found
3. **Virtual Scrolling Support** - Extracts all devices, not just visible ones
4. **Safe Execution** - Includes error handling and depth limits to prevent page lockups

#### Data Storage

- **Device Registry** (`UNIFI_DEVICE_REGISTRY`) - Stores ID to name mappings
- **LocalStorage** - Persists registry across browser sessions
- **No Cloud Sync** - Your data never leaves your device

#### Search Algorithm

- Searches both loaded icons and registry entries
- Case-insensitive matching on device names and IDs
- Limits results to 100 items for performance
- Real-time filtering as you type

## 💡 Why I Made This

As a UniFi network administrator, I found myself constantly scrolling through hundreds of device icons trying to find the right one. The UniFi portal's icon selection interface is functional, but searching by device name would be much more efficient.

This tool was created to:

- **Save time** - Find device icons instantly by name instead of scrolling
- **Build a knowledge base** - Create a personal registry of device names
- **Stay organized** - Keep track of device icons you've used
- **Work offline** - No internet required after initial setup (except for icon images)

## 🎨 Screenshots

### Main Interface
- Clean, modern dark mode interface
- Collapsible instructions section
- Sticky search bar for easy access
- Real-time device count display

### Search Results
- Grid layout with device icons
- Click to copy device names
- Quick access to device IDs and URLs

## 🔒 Privacy & Security

- **100% Local** - All data stays on your device
- **No Tracking** - No analytics, no external requests
- **No Authentication** - No login required
- **Open Source** - Review the code yourself

## 🛠️ Browser Compatibility

- ✅ Chrome/Edge (Chromium) - Full support
- ✅ Firefox - Full support
- ✅ Safari - Full support
- ✅ Opera - Full support

**Note:** The bookmarklet requires a modern browser with JavaScript enabled.

## 📝 File Structure

```
unifi-icon-browser/
├── unifi-icon-browser.html  # Single-file application
└── README.md                # This file
```

That's it! Everything is in one HTML file for maximum portability.

## 🤝 Contributing

Contributions are welcome! Here are some ways you can help:

- 🐛 Report bugs
- 💡 Suggest new features
- 📝 Improve documentation
- 🔧 Submit pull requests

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- **Ubiquiti** - For creating the UniFi ecosystem
- **The Community** - For feedback and suggestions

## 📞 Support

- **Issues** - Report bugs or request features on GitHub Issues
- **Discussions** - Ask questions in GitHub Discussions

## 🗺️ Roadmap

Future improvements may include:

- [ ] Export device registry to JSON file
- [ ] Import device registry from JSON file
- [ ] Bulk icon operations
- [ ] Device icon favorites
- [ ] Custom device name editing
- [ ] Dark/light theme toggle
- [ ] Keyboard shortcuts

## ⚠️ Disclaimer

This tool is not affiliated with or endorsed by Ubiquiti Inc. It is an independent, community-driven project. Use at your own discretion.

---

**Made with ❤️ for the UniFi community**

If you find this tool useful, please consider giving it a ⭐ on GitHub!

