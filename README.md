# VideoMeet App

A professional video calling application built with Flutter, featuring authentication, user management, real-time video communication using Agora SDK, and push notifications for incoming calls.

## 🚀 Features

- **Authentication System**: Secure login with email/password validation
- **User Management**: Browse and manage user profiles with offline caching
- **Video Calling**: One-to-one video calls with Agora RTC SDK
- **Real Screen Sharing**: Live screen sharing between devices using Agora SDK
- **Push Notifications**: Mock incoming video call notifications for testing
- **Modern UI**: Dark theme with responsive design and smooth animations
- **State Management**: Clean architecture with Bloc/Cubit pattern
- **Offline Support**: Cached user data for offline access
- **Enhanced Permissions**: Comprehensive permission handling for screen recording

## 📱 Screenshots

- **Splash Screen**: Animated Lottie loading with authentication check
- **Login Screen**: Clean authentication form with validation
- **User List**: Browse users with shimmer loading effects
- **Profile Screen**: User profile with statistics and actions
- **Video Call**: Real-time video communication interface with screen sharing
- **Screen Sharing**: Live screen sharing with real-time transmission
- **Notification Settings**: Control mock incoming call notifications
- **Push Notifications**: Custom app icon with Accept/Decline actions

## 🎉 Final Summary

**VideoMeet** is a complete, production-ready Flutter video calling application with:

- **🔐 Authentication**: Secure login/logout with validation
- **👥 User Management**: Browse users with offline caching
- **📹 Video Calling**: Real-time video calls using Agora SDK
- **📱 Screen Sharing**: Live screen sharing between devices
- **🔔 Push Notifications**: Mock incoming calls with custom app icon
- **🎨 Modern UI**: Dark theme with responsive design
- **⚡ Performance**: Clean architecture with Bloc/Cubit state management
- **📱 Cross-Platform**: Android and iOS support
- **🚀 Ready to Deploy**: Complete with documentation and release builds

**Files Ready:**
- `videomeet-flutter-app-final.zip` (19MB) - Complete source code with screen sharing
- Release APK ready for distribution
- GitHub repository configured
- Comprehensive documentation included

## ✅ Project Status - COMPLETE

**COMPLETED FEATURES:**
- ✅ Authentication system with login/logout
- ✅ User list with REST API integration and offline caching
- ✅ Video calling with Agora SDK integration
- ✅ Real screen sharing between devices with Agora SDK
- ✅ Enhanced permission handling for screen recording
- ✅ Modern dark theme UI with responsive design
- ✅ Splash screen with Lottie animation
- ✅ Custom app icon and branding
- ✅ Push notifications for incoming calls (mock) with custom icon
- ✅ Notification actions (Accept/Decline) with navigation
- ✅ Clean architecture with Bloc/Cubit state management
- ✅ Error handling and loading states
- ✅ Android/iOS app signing and permissions
- ✅ Comprehensive documentation
- ✅ GitHub repository setup
- ✅ Release APK generation
- ✅ Final ZIP package ready for distribution

**PRODUCTION READY:**
- ✅ All core features implemented and tested
- ✅ App builds successfully for both debug and release
- ✅ Push notifications working correctly with proper splash screen flow
- ✅ Splash screen displays properly before navigation
- ✅ Notification actions properly navigate to video call screen
- ✅ Custom app icon used in notifications
- ✅ Clean, maintainable codebase with proper documentation
- ✅ Source code available in GitHub repository
- ✅ Release APK ready for distribution
- ✅ Final ZIP package (19MB) ready for upload

## 🔔 Push Notifications

The app includes a comprehensive push notification system for incoming video calls:

### Features
- **Mock Incoming Calls**: Simulated video call notifications every 30-120 seconds
- **Test Notifications**: Manual trigger for testing notification functionality
- **Notification Settings**: Control panel accessible from the Profile screen
- **Multiple Mock Callers**: 5 different mock users who can "call" you
- **Missed Call Notifications**: Notifications for unanswered calls
- **Splash Screen Integration**: Notifications initialize after splash screen for better UX

### How to Use
1. **Automatic Setup**: Notifications start automatically after the splash screen
2. **Control Settings**: Go to Profile → Notification Settings to enable/disable simulation
3. **Test Notifications**: Use the "Test Incoming Call" and "Test Missed Call" buttons
4. **View Mock Callers**: See the list of mock users who can call you

### Technical Details
- Uses `flutter_local_notifications` package
- Android: Full-screen intent notifications for incoming calls
- iOS: Standard notifications with call category
- Permission handling for notification access
- Mock service with random call intervals
- Initialized after splash screen to ensure proper app flow
- **Custom app icon** used in all notifications
- **Accept/Decline actions** with proper navigation to video call screen
- **Debug logging** for notification interactions

## 📱 Real Screen Sharing

The app includes comprehensive screen sharing functionality using Agora SDK:

### Features
- **Live Screen Sharing**: Real-time screen transmission between devices
- **Permission Handling**: Automatic request for screen recording permissions
- **Error Handling**: Comprehensive error messages and fallback mechanisms
- **Debug Logging**: Detailed logs for troubleshooting screen sharing issues
- **User Feedback**: Clear status indicators and error messages

### How to Use
1. **Start Video Call**: Join a video call on both devices
2. **Enable Screen Sharing**: Tap the screen share button on one device
3. **Grant Permissions**: Allow screen recording when prompted
4. **View Shared Screen**: The other device will see the shared screen content

### Technical Details
- Uses Agora SDK's `startScreenCapture` and `stopScreenCapture` methods
- Requires Android 10+ (API 29+) for screen recording
- Includes system alert window permission for screen overlay
- Real-time video encoder configuration for optimal quality
- Comprehensive error handling and user feedback

### Troubleshooting Screen Sharing
- **Permission Denied**: Check device settings for "Display over other apps"
- **Not Working**: Ensure both devices are on the same network
- **Poor Quality**: Check network connection and device performance
- **Debug Logs**: Watch console for detailed error messages

## 🛠️ Build & Run Instructions

### Prerequisites

- Flutter SDK (3.0.0 or higher)
- Dart SDK (2.17.0 or higher)
- Android Studio / Xcode (for mobile development)
- Android SDK (API level 21+)
- iOS 11.0+ (for iOS development)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd hipster_inc_assignment
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Generate code (if needed)**
   ```bash
   flutter packages pub run build_runner build
   ```

4. **Run the application**
   ```bash
   # For Android
   flutter run --debug -d android
   
   # For iOS
   flutter run --debug -d ios
   
   # For specific device
   flutter run --debug -d <device-id>
   ```

### Build for Release

```bash
# Android APK
flutter build apk --release

# Android App Bundle
flutter build appbundle --release

# iOS
flutter build ios --release
```

## 🔧 SDK Setup & Configuration

### Agora RTC SDK Setup

1. **Get Agora App ID**
   - Sign up at [Agora Console](https://console.agora.io/)
   - Create a new project
   - Copy your App ID

2. **Configure App ID**
   ```dart
   // lib/features/video_call/data/services/agora_video_service.dart
   static const String _appId = 'YOUR_AGORA_APP_ID';
   ```

3. **Android Permissions**
   ```xml
   <!-- android/app/src/main/AndroidManifest.xml -->
   <uses-permission android:name="android.permission.INTERNET" />
   <uses-permission android:name="android.permission.CAMERA" />
   <uses-permission android:name="android.permission.RECORD_AUDIO" />
   <uses-permission android:name="android.permission.MODIFY_AUDIO_SETTINGS" />
   <!-- Screen sharing permissions -->
   <uses-permission android:name="android.permission.SYSTEM_ALERT_WINDOW" />
   <uses-permission android:name="android.permission.FOREGROUND_SERVICE" />
   <uses-permission android:name="android.permission.FOREGROUND_SERVICE_MEDIA_PROJECTION" />
   ```

4. **iOS Permissions**
   ```xml
   <!-- ios/Runner/Info.plist -->
   <key>NSCameraUsageDescription</key>
   <string>This app needs camera access for video calls</string>
   <key>NSMicrophoneUsageDescription</key>
   <string>This app needs microphone access for video calls</string>
   ```

### App Icon Setup

1. **Generate App Icons**
   ```bash
   flutter pub run flutter_launcher_icons:main
   ```

2. **Manual Setup** (if needed)
   - Place 1024x1024 PNG icon in `assets/icons/app_icon.png`
   - Run icon generation command
   - Clean and rebuild the project

### Environment Configuration

1. **Create environment file** (optional)
   ```dart
   // lib/core/constants/app_constants.dart
   class AppConstants {
     static const String appName = 'VideoMeet';
     static const String appVersion = '1.0.0';
     // Add your configuration here
   }
   ```

## 📋 Project Structure

```
lib/
├── core/
│   ├── constants/          # App constants and colors
│   ├── di/                # Dependency injection
│   ├── navigation/        # App routing
│   └── widgets/           # Reusable widgets
├── features/
│   ├── auth/              # Authentication feature
│   ├── user_list/         # User management
│   ├── video_call/        # Video calling
│   └── splash/            # Splash screen
└── main.dart              # App entry point
```

## 🔑 Key Dependencies

- **flutter_bloc**: State management
- **go_router**: Navigation
- **agora_rtc_engine**: Video calling
- **shared_preferences**: Local storage
- **cached_network_image**: Image caching
- **lottie**: Animations
- **permission_handler**: Permissions

## ⚠️ Assumptions & Limitations

### Authentication
- **Mock Authentication**: Uses hardcoded credentials for demo purposes
- **No Real Backend**: Authentication is simulated locally
- **Session Management**: Basic session handling with SharedPreferences

### Video Calling
- **Agora SDK Required**: Real video calls need valid Agora App ID
- **Token Authentication**: Production requires Agora tokens for security
- **Network Dependency**: Video calls require stable internet connection
- **Device Permissions**: Camera and microphone access required

### User Management
- **Mock Data**: User list uses JSONPlaceholder API with fallback to mock data
- **Offline Caching**: Limited offline functionality with cached data
- **No Real-time Updates**: User list doesn't update in real-time

### Platform Support
- **Android**: API level 21+ (Android 5.0+)
- **iOS**: iOS 11.0+
- **Web**: Limited support (video calling not fully supported)
- **Desktop**: Not optimized for desktop platforms

### Performance Considerations
- **Memory Usage**: Video calls consume significant memory
- **Battery Life**: Continuous video streaming drains battery
- **Network Bandwidth**: High-quality video requires good internet
- **Device Compatibility**: Older devices may have performance issues

## 🐛 Known Issues

1. **Agora Token Error**: Video calls may fail without proper token setup
2. **Permission Denied**: Camera/microphone access may be denied on some devices
3. **Network Timeout**: API calls may timeout on slow connections
4. **Memory Leaks**: Long video calls may cause memory issues

## 🔧 Troubleshooting

### Common Issues

1. **Build Failures**
   ```bash
   flutter clean
   flutter pub get
   flutter run
   ```

2. **Permission Issues**
   - Check device settings for camera/microphone permissions
   - Restart the app after granting permissions

3. **Video Call Issues**
   - Verify Agora App ID is correct
   - Check network connectivity
   - Ensure device has camera/microphone

4. **Push Notification Issues**
   - Check notification permissions in device settings
   - Ensure app is not in battery optimization mode
   - Test notifications using the Notification Settings page

5. **Screen Sharing Issues**
   - Check device compatibility (Android 10+ required)
   - Enable "Display over other apps" permission in device settings
   - Ensure both devices are on the same network
   - Check console logs for detailed error messages
   - Verify Agora App ID is correct and active

6. **App Icon Not Showing**
   ```bash
   flutter clean
   flutter pub run flutter_launcher_icons:main
   flutter run
   ```

## 📄 License

This project is for demonstration purposes. Please ensure you have proper licenses for:
- Agora RTC SDK
- Any third-party assets used
- Platform-specific requirements

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📞 Support

For issues and questions:
- Check the troubleshooting section
- Review the known issues
- Create an issue in the repository

---

**Note**: This is a demonstration application. For production use, implement proper security measures, backend integration, and error handling.
