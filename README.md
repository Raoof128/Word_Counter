# 🧮 Exact Word Counter

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/Raoof128/Word_Counter/graphs/commit-activity)

A high-precision, feature-rich Progressive Web App (PWA) for real-time text analysis. Built with vanilla JavaScript, fully offline-capable, and designed with accessibility in mind.

## ✨ Features

### 📊 Comprehensive Text Analysis
- **Word Count**: Accurate word counting with Smart and Strict modes
- **Character Count**: Track characters with and without spaces
- **Sentence Count**: Intelligent sentence detection including CJK punctuation
- **Line Count**: Accurate line counting
- **Unique Words**: Count distinct words in your text
- **Average Word Length**: Calculate mean word length with decimal precision
- **Longest Word**: Identify the longest word (with smart truncation)
- **Reading Time**: Estimated reading time (200 WPM)
- **Word Frequency**: Top 10 most used words with occurrence count

### 🎨 User Experience
- **Dark Mode**: Beautiful dark theme with persistent preference
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile
- **Real-time Updates**: Instant statistics as you type
- **Keyboard Shortcuts**: Power user features for efficiency
- **Toast Notifications**: Clear visual feedback for actions
- **Offline Support**: Full functionality without internet connection

### ⚙️ Configurable Options
- **Smart Mode**: Unicode-aware word segmentation using `Intl.Segmenter`
- **Strict Mode**: Whitespace-based word splitting
- **Count Numbers**: Toggle numeric value counting
- **Hyphenated Words**: Treat hyphenated terms as single or multiple words
- **Reading Time Toggle**: Show/hide reading time estimate

### 📋 Productivity Features
- **Copy Statistics**: One-click copy all stats to clipboard
- **Clear Text**: Quick text clearing with confirmation
- **Auto-save Preferences**: All settings persist across sessions
- **PWA Installation**: Install as native app on any device

### ♿ Accessibility
- **ARIA Labels**: Complete screen reader support
- **Keyboard Navigation**: Full keyboard accessibility
- **Focus Indicators**: Clear visual focus states
- **Live Regions**: Screen reader announcements for stats

## 🚀 Quick Start

### Option 1: Open Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/Raoof128/Word_Counter.git
   cd Word_Counter
   ```

2. Open `index.html` in your browser:
   ```bash
   # On macOS
   open index.html

   # On Linux
   xdg-open index.html

   # On Windows
   start index.html
   ```

### Option 2: Serve with Local Server
```bash
# Using Python 3
python3 -m http.server 8000

# Using Node.js (npx)
npx serve

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000` in your browser.

### Option 3: Install as PWA
1. Open the app in a modern browser (Chrome, Edge, Safari)
2. Click the install prompt or use browser's "Install App" option
3. Enjoy native-like experience with offline support

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Alt+D` | Toggle dark/light mode |
| `Alt+C` | Clear text (with confirmation) |
| `Alt+S` | Copy statistics to clipboard |
| `Alt+H` | Show keyboard shortcuts help |
| `Ctrl+A` | Select all text |

## 🎯 Use Cases

- **Content Writers**: Track word count for articles, blog posts, and essays
- **Students**: Monitor assignment length and reading time
- **Copywriters**: Ensure content meets character limits
- **Translators**: Analyze text complexity and word frequency
- **Social Media**: Stay within platform character limits
- **SEO Specialists**: Optimize content length and word density
- **Developers**: Analyze code documentation and comments
- **Researchers**: Study text patterns and word usage

## 🧪 Testing

The application includes a comprehensive test checklist in the original README. To verify functionality:

**Test Configuration:**
- Mode: `Smart`
- Count numbers: `ON`
- Treat hyphenated terms as one word: `ON`

**Test Input:**
```
This state-of-the-art PWA is test #1. Don't you agree? It works in 日本語 too… What a result!
```

**Expected Output:**
| Metric | Expected Value |
|--------|----------------|
| Words | 20 |
| Sentences | 4 |
| Lines | 1 |
| Top word | `this` (2) |

## 🏗️ Architecture

### Technology Stack
- **Frontend**: Vanilla JavaScript (ES6+)
- **Styling**: CSS3 with Custom Properties
- **PWA**: Service Workers, Web App Manifest
- **APIs**: Intl.Segmenter, Clipboard API, LocalStorage

### File Structure
```
Word_Counter/
├── index.html              # Main application (HTML, CSS, JS)
├── manifest.webmanifest    # PWA configuration
├── service-worker.js       # Offline support & caching
├── README.md              # Documentation
├── LICENSE                # MIT License
├── CONTRIBUTING.md        # Contribution guidelines
├── CHANGELOG.md           # Version history
└── .gitignore            # Git ignore rules
```

### Key Features Implementation

#### Smart Word Counting
- Uses `Intl.Segmenter` API for Unicode-aware word boundaries
- Falls back to regex for older browsers
- Filters emojis and special characters
- Handles CJK languages correctly

#### PWA Capabilities
- Offline-first architecture with Service Workers
- Installable on all platforms
- Automatic cache management
- Update notifications

#### Performance
- No external dependencies (zero bundle size)
- Debounced screen reader announcements
- Efficient DOM updates
- Minimal repaints

## 🔒 Privacy & Security

- **No Data Collection**: All processing happens locally in your browser
- **No Analytics**: Your text never leaves your device
- **No Cookies**: No tracking or third-party services
- **Open Source**: Fully auditable code

## 🌐 Browser Support

| Browser | Minimum Version | Notes |
|---------|----------------|-------|
| Chrome | 90+ | Full support |
| Edge | 90+ | Full support |
| Safari | 14+ | Full support |
| Firefox | 88+ | Full support (no Intl.Segmenter, uses fallback) |

### Required APIs
- ES6+ JavaScript features
- CSS Custom Properties
- LocalStorage API
- Service Workers (for PWA features)
- Clipboard API (for copy feature)

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details on:
- Code of Conduct
- Development setup
- Pull request process
- Coding standards

## 📝 Changelog

See [CHANGELOG.md](CHANGELOG.md) for a detailed version history.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Icon: Abacus emoji (🧮)
- Inspired by the need for a privacy-focused, offline-capable word counter
- Built with modern web standards and best practices

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/Raoof128/Word_Counter/issues)
- **Discussions**: [GitHub Discussions](https://github.com/Raoof128/Word_Counter/discussions)
- **Security**: See [SECURITY.md](SECURITY.md) for reporting vulnerabilities

## 🎖️ Recognition

If you find this project useful, please consider:
- ⭐ Starring the repository
- 🐛 Reporting bugs
- 💡 Suggesting features
- 🤝 Contributing code
- 📢 Sharing with others

---

**Made with ❤️ for the open source community**

*No tracking • No ads • No data collection • 100% free forever*
