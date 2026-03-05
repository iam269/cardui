# Card UI - Credit Card Design

A beautiful Flutter UI challenge displaying a stylized credit card with modern design elements.

## Features

- Credit card UI with logo and chip
- Card number display: 5678 4356 0126 7800
- Cardholder name: AKSHIT MADAN
- Green gradient background with shadow effects
- Responsive design

## Running the App

### Web (Browser)
```bash
# Development mode
flutter run -d chrome

# Production build
flutter build web
```

The built app will be in `build/web/` folder.

To serve locally:
```bash
cd build/web
python -m http.server 8000
```
Then open http://localhost:8000

### Android
```bash
flutter run -d android
```

### iOS (macOS only)
```bash
flutter run -d ios
```

## Requirements

- Flutter SDK (latest version recommended)
- Chrome browser (for web development)
- Android Studio or VS Code with Flutter extension

## Project Structure

```
lib/
├── main.dart          # App entry point
├── pages/
│   ├── home.dart      # Home screen with card container
│   └── content.dart   # Card design implementation
└── utils/
    ├── colors.dart    # Color definitions and shadows
    └── text.dart      # Custom text widget
```

## Dependencies

- `google_fonts: ^6.1.0` - For custom typography
- `cupertino_icons: ^1.0.2` - iOS style icons

---

This is a Flutter UI challenge project demonstrating credit card design implementation.
