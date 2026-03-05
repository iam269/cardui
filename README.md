# Card UI - Credit Card Design Challenge

A sophisticated Flutter UI project that showcases a modern credit card design with elegant visual effects and professional typography. This project demonstrates advanced Flutter widgets, custom styling, and responsive layout techniques.

## 🎯 Project Overview

This Flutter UI challenge focuses on creating a visually appealing credit card interface that mimics real-world payment card designs. The implementation features:

- **Realistic Card Design**: A credit card with authentic styling including chip, logo, and card details
- **Modern Typography**: Custom fonts using Google Fonts (Source Code Pro for card numbers, Mada for italic text)
- **Visual Effects**: Sophisticated shadow effects and gradient backgrounds
- **Responsive Layout**: Adapts to different screen sizes using MediaQuery

## 📱 Features

### Card Components
- **Logo Display**: Custom logo asset positioned at the top-left
- **EMV Chip**: Integrated circuit chip graphic for authenticity
- **Card Number**: 16-digit formatted number (5678 4356 0126 7800)
- **Cardholder Name**: Displayed in uppercase (AKSHIT MADAN)
- **Tagline**: "it's where you want to be" in elegant italic font

### Visual Design
- **Background**: Soft green gradient (#4CAF50 family)
- **Shadows**: Dual-layer shadow system for depth
- **Decorative Elements**: Circular background patterns with transparency
- **Color Palette**: 
  - Primary: Green shades (200-900)
  - Text: Dark grey (#424242)
  - Accents: White with opacity variations

## 🏗️ Project Architecture

```
lib/
├── main.dart                 # Application entry point
├── pages/
│   ├── home.dart            # Main scaffold with card container
│   └── content.dart        # Card UI implementation with Stack widgets
└── utils/
    ├── colors.dart          # Color definitions and BoxShadow configurations
    └── text.dart           # Custom modifiedtext widget with Google Fonts
```

### Key Files Description

#### lib/main.dart
- MaterialApp configuration
- Theme setup with custom primary color
- Debug banner disabled
- Routes to Home page

#### lib/pages/home.dart
- Scaffold with green background
- Centered card container (250px height)
- Card positioned at bottom with margin
- Custom shadow effects applied

#### lib/pages/content.dart
- Stack-based layout for layered design
- Two decorative circular backgrounds
- Image assets for logo and chip
- Google Fonts integration for typography

#### lib/utils/colors.dart
- AppColors class with static color definitions
- bgColor: green.shade200 for main background
- shadows: List of BoxShadow configurations

#### lib/utils/text.dart
- modifiedtext StatelessWidget
- GoogleFonts.mada integration
- Custom color, size, and italic styling

## 🚀 Getting Started

### Prerequisites
- Flutter SDK 3.0+ (recommended latest version)
- Dart SDK 3.0+
- Chrome browser (for web development)
- Android Studio or VS Code with Flutter extension

### Installation

1. **Clone the repository:**
```bash
git clone <repository-url>
cd cardui
```

2. **Install dependencies:**
```bash
flutter pub get
```

3. **Run the application:**

#### Web (Browser)
```bash
# Development with hot reload
flutter run -d chrome

# Production build
flutter build web
```

#### Android
```bash
flutter run -d android
```

#### iOS (macOS only)
```bash
flutter run -d ios
```

### Running Tests
```bash
flutter test
```

## 📦 Dependencies

### Required Packages
```yaml
dependencies:
  flutter:
    sdk: flutter
  google_fonts: ^6.1.0
  cupertino_icons: ^1.0.2
```

### Asset Requirements
```
assets/
├── chip.png    # EMV chip graphic (51KB)
└── logo.png   # Card logo (81KB)
```

## 🔧 Configuration

### Web Platform
- Responsive viewport meta tags in index.html
- PWA manifest configuration
- Favicon assets for various sizes

### Android Platform
- Standard Flutter Android configuration
- Material Design support
- Night mode styles included

### iOS Platform
- iOS-specific asset catalogs
- Launch screen configurations
- Cupertino icon support

## 🖥️ Usage Examples

### Development Server
```bash
# Start web development server
flutter run -d chrome

# Available hot reload commands:
# R - Hot restart
# h - Help
# c - Clear screen
# q - Quit
```

### Building for Production

#### Web Build
```bash
flutter build web --release
# Output: build/web/
```

#### Android APK
```bash
flutter build apk --release
# Output: build/app/outputs/flutter-apk/app-release.apk
```

#### iOS Build (macOS only)
```bash
flutter build ios --release --no-codesign
# Output: build/ios/iphoneos/
```

## 📂 Output Files

After building, the following outputs are generated:

- **Web**: `build/web/index.html`, `build/web/main.dart.js`
- **Android APK**: `build/app/outputs/flutter-apk/app.apk`
- **iOS**: `build/ios/iphoneos/Runner.app`

## 🎨 Design Details

### Color Scheme
| Element | Color | Hex Code |
|---------|-------|----------|
| Background | Green 200 | #A5D6A7 |
| Primary Dark | Green 900 | #1B5E20 |
| Text Primary | Grey 900 | #212121 |
| Text Secondary | Grey 700 | #616161 |
| Shadow Light | White 50% | #FFFFFF80 |
| Shadow Dark | Green 900 20% | #1B5E2033 |

### Typography
| Element | Font | Size | Weight |
|---------|------|------|--------|
| Card Number | Source Code Pro | 24px | Bold (700) |
| Cardholder Name | Source Code Pro | 20px | SemiBold (600) |
| Tagline | Mada | 14px | Normal, Italic |

### Layout Specifications
- Card Height: 250px
- Card Margin: 18px horizontal, 100px bottom
- Logo Position: top: 25px, left: 15px
- Chip Position: right: 10px
- Card Number Position: bottom: 30px, left: 15px

## 🔍 Technical Implementation

### Widgets Used
- `Scaffold` - Main screen structure
- `Container` - Card container with decorations
- `Stack` - Layered card elements
- `Positioned` - Element placement
- `Image.asset` - Logo and chip display
- `Text` - Card text information

### Advanced Techniques
- `BoxShadow` with spread and blur radius
- `Colors.withOpacity()` for transparency
- `MediaQuery.of(context).size.width` for responsiveness
- `GoogleFonts` for custom typography

## 📝 License

This project is created for educational purposes as a Flutter UI challenge.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📚 Additional Resources

- [Flutter Documentation](https://flutter.dev/docs)
- [Google Fonts Package](https://pub.dev/packages/google_fonts)
- [Flutter Widget Catalog](https://flutter.dev/docs/development/ui/widgets)

---

## 🚀 Deploy to GitHub Pages

### Option 1: Automatic Deployment (Recommended)

This project includes a GitHub Actions workflow that automatically builds and deploys to GitHub Pages when you push to the `main` branch.

**Steps:**

1. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Navigate to Settings → Pages
   - Under "Build and deployment", select "Deploy from a branch"
   - Select branch: `gh-pages` and folder: `/ (root)`
   - Click Save

2. **Push to main branch:**
   ```bash
   git add .
   git commit -m "Add GitHub Pages deployment"
   git push origin main
   ```

3. **The workflow will:**
   - Build the Flutter web app
   - Deploy to `gh-pages` branch
   - Your site will be available at: `https://<username>.github.io/<repo>/`

### Option 2: Manual Deployment

1. **Build the web app:**
   ```bash
   flutter build web --release
   ```

2. **Create gh-pages branch:**
   ```bash
   git checkout -b gh-pages
   git add build/web -f
   git commit -m "Deploy to GitHub Pages"
   git push origin gh-pages
   ```

3. **Enable Pages in GitHub:**
   - Settings → Pages
   - Source: Select "gh-pages" branch
   - Save

### Option 3: Using Firebase Hosting (Alternative)

```bash
# Install Firebase CLI
npm install -g firebase-tools

# Initialize Firebase
firebase init hosting

# Deploy
firebase deploy
```

---

**Built with ❤️ using Flutter**

Created as part of the Flutter UI Challenges series.
