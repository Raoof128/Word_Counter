# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2025-01-14

### Added
- **Dark Mode**: Complete dark theme with persistent user preference
- **Additional Statistics**:
  - Unique words count
  - Average word length calculation
  - Longest word detection
- **Productivity Features**:
  - Clear text button with confirmation
  - Copy statistics to clipboard
  - Keyboard shortcuts (Alt+D, Alt+C, Alt+S, Alt+H)
  - Help dialog for keyboard shortcuts
- **PWA Enhancements**:
  - Install prompt with dismiss option
  - Offline indicator banner
  - Better service worker with cache management
- **User Preferences**:
  - LocalStorage persistence for all settings
  - Auto-save on configuration changes
  - Restore preferences on page load
- **UI Improvements**:
  - Toast notifications for user actions
  - Animated notification system
  - Better button styling and hover states
  - Responsive header layout
  - Icon buttons for actions
- **Accessibility**:
  - Keyboard hints for screen readers
  - ARIA labels for all interactive elements
  - Better focus indicators

### Changed
- Improved responsive design with better mobile layout
- Enhanced CSS with more variables for theming
- Better service worker with proper cache cleanup
- Updated manifest with inline SVG icons
- Improved statistics grid layout to accommodate new metrics

### Fixed
- Line count now correctly returns 0 for empty text
- Textarea overflow with proper box-sizing
- Service worker cache paths (relative vs absolute)
- PWA manifest icon references

## [1.0.0] - 2025-01-13

### Added
- Initial release with core functionality
- **Text Analysis**:
  - Word count with Smart and Strict modes
  - Character count (with and without spaces)
  - Sentence count
  - Line count
  - Reading time estimation
  - Top 10 word frequency analysis
- **Smart Mode Features**:
  - Unicode-aware word segmentation using Intl.Segmenter
  - Fallback regex for older browsers
  - Support for CJK languages
  - Emoji filtering
  - Hyphenated word handling
- **Configuration Options**:
  - Toggle between Smart and Strict modes
  - Count/ignore numbers
  - Hyphenated words as one or multiple
  - Show/hide reading time
- **PWA Support**:
  - Service worker for offline functionality
  - Web app manifest
  - Installable as native app
- **Accessibility**:
  - Screen reader support with ARIA labels
  - Debounced live region announcements
  - Keyboard accessible controls
  - Focus management
- **UI/UX**:
  - Clean, modern design
  - Real-time statistics updates
  - Responsive layout
  - Statistics grid with visual hierarchy
  - Word frequency list
- **Privacy**:
  - 100% client-side processing
  - No data collection
  - No external dependencies
  - No analytics

### Technical Details
- Built with vanilla JavaScript (ES6+)
- CSS3 with Custom Properties
- No build process required
- Zero external dependencies
- Works offline after first visit
- Service Worker v1 implementation

---

## Version History Summary

- **2.0.0** (2025-01-14): Major feature update with dark mode, enhanced statistics, productivity tools, and improved PWA capabilities
- **1.0.0** (2025-01-13): Initial release with core word counting and text analysis features

---

## Upgrade Notes

### Upgrading to 2.0.0
- Clear your browser cache to see the new features
- The app will automatically update via service worker
- All previous preferences will be migrated
- No breaking changes to core functionality

## Future Roadmap

### Planned Features
- [ ] Export statistics to CSV/JSON
- [ ] Readability score calculation
- [ ] Multi-language UI support
- [ ] Custom word lists and stopwords
- [ ] Text comparison tool
- [ ] Character encoding analysis
- [ ] Paragraph statistics
- [ ] Print functionality
- [ ] Cloud sync for preferences (optional)
- [ ] Browser extension version

### Under Consideration
- PDF import support
- Rich text formatting support
- Grammar and spelling suggestions
- Writing style analysis
- Markdown support
- Multiple document tabs

---

For detailed information about each release, see the [GitHub Releases](https://github.com/Raoof128/Word_Counter/releases) page.
