# Jump

A location-based notification iOS app that alerts users when they arrive at their destination. Perfect for bus travelers and commuters who don't want to miss their stop.

## Overview

Jump is a native iOS application that uses GPS tracking and geofencing to notify you when you've reached your destination. Simply pin your destination on the map, and the app will monitor your location in the background and send you a notification when you arrive.

## Features

- **Real-time Location Tracking** - Continuous GPS tracking with background location updates
- **Geofencing** - Automatic arrival detection using region monitoring
- **Push Notifications** - Get notified when you enter or exit your destination area
- **Route Visualization** - View turn-by-turn directions on the map with alternate routes
- **Dark Mode Support** - Adaptive UI that responds to system appearance settings
- **Background Operation** - App works in the background so you can lock your phone

 ## Requirements

- iOS 12.0+
- Xcode 11.0+
- iPhone/iPad device with GPS capabilities
- Location permissions (Always/When In Use)

## Usage

1. **Launch the app** - Grant location permissions when prompted (select "Always Allow" for best experience)
2. **Grant notification permissions** - Allow notifications to receive arrival alerts
3. **Pan the map** to your desired destination location
4. **Tap "Choose Destination"** - The app will:
   - Pin your destination on the map
   - Calculate and display the route
   - Start monitoring your location in the background
5. **Travel to your destination** - Lock your phone and go about your journey
6. **Receive notification** - When you arrive within the destination area, you'll get a "Jumped!" notification
7. **Tap "Reset Destination"** when you're done to clear the route and stop monitoring

## How It Works

Jump uses Apple's CoreLocation framework to monitor your location and detect when you enter a designated geographic region (geofence). The app:

1. Continuously tracks your location with 1-meter precision
2. Creates a circular geofence around your destination
3. Monitors for region entry/exit events
4. Triggers a local push notification when you enter the destination region
5. Runs in the background with minimal battery impact

## Permissions

The app requires the following permissions:

- **Location Services (Always)** - To track your location in the background
- **Notifications** - To alert you when you arrive at your destination

Location permission descriptions in Info.plist:
- "Allows us to use your location to provide you features to notifing you when you arrived to the destination point at traveling by bus."

## Technical Details

### Architecture
- **Pattern**: Model-View-Controller (MVC)
- **UI Framework**: UIKit with Storyboards
- **Language**: Swift

### Key Technologies
- **MapKit** - Map display, annotations, and routing
- **CoreLocation** - GPS tracking and geofencing
- **UserNotifications** - Local push notifications
- **Background Modes** - Location updates and background fetch

## Known Limitations

- App must remain running in the background to receive notifications
- Location accuracy depends on GPS signal strength
- Geofence radius is fixed (determined by the route region)
- Battery usage increases with continuous location tracking

## Privacy

Jump takes your privacy seriously:
- All location data is processed locally on your device
- No data is sent to external servers
- No third-party analytics or tracking
- Location permissions can be revoked at any time in Settings

## Future Enhancements

- [ ] Customizable geofence radius
- [ ] Multiple destination support
- [ ] Saved favorite locations
- [ ] SwiftUI migration
- [ ] iPad optimization
- [ ] Custom notification sounds
- [ ] Route history
- [ ] Estimated arrival time

## Author

**Melisa Öztürk**
- GitHub: [@melisaozturk](https://github.com/melisaozturk)

## Acknowledgments

- Built with Apple's MapKit and CoreLocation frameworks
- Inspired by the need for reliable arrival notifications during bus commutes


