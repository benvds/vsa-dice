# Dice – a very small app

https://dice.verysmall.app

A simple, elegant dice rolling app.

## Features

- **Roll 1-6 Dice**: Add or remove dice with the + and - buttons
- **Smooth Animations**: Staggered rolling animation for multiple dice
- **Cryptographically Secure Random**: Uses `crypto.getRandomValues()` for true randomness
- **Progressive Web App**: Install on your device and use offline
- **Auto-Updates**: Automatic update detection with user notification
- **Dark Mode**: Automatically adapts to your system color scheme
- **Mobile Optimized**: Touch-friendly interface with responsive design
- **Offline First**: Works completely offline after installation

## Installation

### Desktop (Chrome, Edge, Brave)
1. Visit the app in your browser
2. Click the install icon in the address bar (or menu → Install)
3. The app will be added to your applications

### iOS (Safari)
1. Visit the app in Safari
2. Tap the Share button
3. Tap "Add to Home Screen"
4. Tap "Add"

### Android (Chrome)
1. Visit the app in Chrome
2. Tap the menu (⋮)
3. Tap "Install app" or "Add to Home Screen"

## Usage

- **Roll**: Tap the "Roll" button to roll all dice
- **Add Dice**: Tap the + button (up to 6 dice)
- **Remove Dice**: Tap the - button (minimum 1 die)

## Updates

The app automatically checks for updates:
- Every time you open the app
- Every hour while the app is running

When an update is available, you'll see a green notification at the top. Tap it to refresh and get the latest version.

## Development

### Prerequisites
- Node.js (for running a local server)
- Pnpm (for package management)
- Modern web browser

### Running Locally

```bash
pnpm install
pnpm dev
```

Then visit `http://localhost:8787` (or the port shown in terminal).

### Project Structure

```
dice/
├── public/
│   ├── index.html       # Main app file
│   ├── sw.js            # Service worker for PWA functionality
│   ├── manifest.json    # PWA manifest
│   ├── icon.svg         # App icon (SVG)
│   ├── icon-192.png     # App icon (192x192)
│   ├── icon-512.png     # App icon (512x512)
│   └── favicon.ico      # Favicon
└── README.md
```

### Updating the Cache Version

When making changes to the app, increment the cache version in `public/sw.js`:

```javascript
const CACHE_NAME = 'dice-v2'; // Change to v3, v4, etc.
```

This ensures users get the latest version when updates are deployed.

## Technologies Used

- **Vanilla JavaScript**: No frameworks or dependencies
- **Service Workers**: For offline functionality and caching
- **Web Crypto API**: For secure random number generation
- **CSS Grid**: For responsive dice layout
- **PWA Manifest**: For installability

## Browser Support

- Chrome/Edge 67+
- Safari 11.1+
- Firefox 63+
- Opera 54+

## License

MIT
