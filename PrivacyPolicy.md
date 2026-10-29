# Privacy Policy for GPS Audio Recorder (iOS)

**Last Updated:** April 27, 2026

**Effective Date:** April 27, 2026

---

## Introduction

GPS Audio Recorder ("the App") is committed to protecting your privacy. This Privacy Policy explains how information is handled when you use this iOS mobile application.

**Key Points:**
- All data is stored locally on your device
- No data is sent to external servers
- No third-party analytics or tracking
- You have full control over your data

---

## 1. Information Collected

### 1.1 Audio Recordings
- The App records audio through your device's microphone when you explicitly start a recording
- Audio files are saved in AAC format (M4A container)
- Recordings are stored only in the app's private storage on your device

### 1.2 Location Data (GPS Coordinates)
- The App collects GPS coordinates when you start a recording
- Location data is stored in three places for maximum portability:
  1. In the app's local SwiftData database
  2. In the audio file's filename (e.g., Recording_20260120_GPS_5.3647_9.2744.m4a)
  3. As a full GPS path inside the M4A file as `rGPS` metadata atom (v1.6.0+)
     - Contains latitude, longitude, timestamp, and accuracy for each recorded point
     - Stored in a custom iTunes metadata tag (readable by ffprobe, MediaInfo, AtomicParsley)
- GPS coordinates are stored locally and never transmitted
- Location data is used solely to tag recordings with their capture location
- Location names (country, state/province) are resolved entirely offline using embedded geographical boundary data (Natural Earth, Public Domain). No coordinates are ever transmitted to external services for this purpose.

### 1.3 Recording Metadata
- Timestamp (when the recording was created)
- Duration (length of the recording)
- Custom names (if you rename a recording)
- Tags (if you assign tags to recordings)
- Waveform data (for visualization purposes)
- GPS travel path (full GPS track recorded during recording, stored as rGPS metadata atom inside the M4A file)

---

## 2. How Information Is Used

All collected data is used exclusively for the following purposes:

- **Audio Recordings:** To capture, store, and play back your voice memos or field recordings
- **Location Data:** To tag recordings with their capture location for organizational purposes
- **Metadata:** To display, organize, and filter your recordings within the app

---

## 3. Data Storage and Security

### 3.1 Local Storage Only
- **All personal data is stored locally on your device**
- Audio files are saved in the app's Documents directory (`/Documents/Recordings/`)
  - Accessible via Files app and iTunes/Finder file sharing
  - Deleted when app is uninstalled
- GPS coordinates and metadata are stored in SwiftData (fully sandboxed by iOS)
- GPS travel path data is embedded directly inside each M4A file as `rGPS` metadata atom
- **No personal data (audio, GPS, metadata) is transmitted to external servers**

### 3.2 Data Access
- Only you have access to your recordings and location data
- The App does not share, sell, or transmit your data to third parties
- Data remains on your device unless you explicitly share recordings using the built-in share function

### 3.3 File Sharing
- When you use the "Share" feature, recordings are shared via iOS's standard UIActivityViewController
- You choose which apps (Messages, Mail, AirDrop, etc.) receive the shared files
- Shared files include GPS coordinates and recording time:
  - In the filename (if GPS was available during recording)
  - As embedded `rGPS` metadata inside the M4A file (v1.6.0+)
- Example shared filename: Recording_20260120_GPS_5.3647_9.2744.m4a
- Recipients can extract GPS location data from shared files using metadata tools (e.g., ffprobe, MediaInfo, AtomicParsley)
- The app warns users about embedded GPS metadata before sharing (v1.6.1)

---

## 4. Third-Party Services

The App uses the following third-party components:

### 4.1 Apple CoreLocation
- **Purpose:** To obtain GPS coordinates for location tagging
- **Data Collected:** Latitude and longitude at the time of recording
- **Data Sharing:** Location data is NOT shared with Apple or any third party
- **Privacy Policy:** https://www.apple.com/privacy/

### 4.2 Apple MapKit
- **Purpose:** To display recordings on a map
- **Data Collected:** Map tiles are downloaded from Apple's servers based on your map view
- **Data Transmitted:** Map tile requests (coordinates of visible map area) are sent to Apple servers
- **Data NOT Shared:** Your recording locations, audio files, or GPS coordinates are never transmitted
- **Privacy Policy:** https://www.apple.com/privacy/

### 4.3 Natural Earth (Offline Geocoding)
- **Purpose:** To display country and state/province names for recording locations
- **Data Processing:** Entirely offline – embedded geographical boundary data is included in the app
- **Data Transmitted:** None – no coordinates are sent to any server for geocoding
- **License:** Public Domain (no restrictions)

### 4.4 AVFoundation (M4A Metadata Processing)
- **Purpose:** To embed and read GPS (and GPS travel path) data (`rGPS` atom) inside M4A audio files
- **Data Processing:** Entirely local – reads and writes metadata atoms within audio files on your device
- **Data Transmitted:** None – no audio files or metadata are sent to any server
- **Framework:** Apple's native AVFoundation framework

**Important:** The App does not use analytics, crash reporting, or advertising services.

---

## 5. Permissions Explained

The App requires the following iOS permissions:

| Permission | Purpose | When Used |
|------------|---------|-----------|
| `NSMicrophoneUsageDescription` | To capture audio recordings | When you tap the record button |
| `NSLocationWhenInUseUsageDescription` | To obtain precise GPS coordinates | When you start a recording |
| `UIBackgroundModes: audio` | To continue recording when app is in background | During active recordings |
| `UIBackgroundModes: location` | To record GPS while recording in background | During active recordings |

All permissions are requested only when needed and can be revoked at any time in iOS Settings.

---

## 6. Data Retention and Deletion

### 6.1 Data Retention
- Recordings and location data are stored indefinitely until you delete them
- The App does not automatically delete any data

### 6.2 How to Delete Your Data
You can delete your data at any time:
- **Delete Individual Recordings:** Tap recording → Delete button
- **Delete Multiple Recordings:** Use multi-select mode in Archive → tap delete icon
- **Delete All Data:** Uninstall the app (this removes all recordings, location data, and metadata)

### 6.3 Complete Data Removal
To completely remove all app data:
1. iOS Settings → General → iPhone Storage → GPS Audio Recorder
2. Tap "Delete App"
3. Or: Long-press app icon on Home Screen → Remove App → Delete App

---

## 7. Children's Privacy

The App does not knowingly collect personal information from children under 13. If you are under 13, please do not use the App without parental consent.

---

## 8. Changes to This Privacy Policy

This Privacy Policy may be updated from time to time. Changes will be posted within the App and on this page with an updated "Last Updated" date.

Continued use of the App after changes constitutes acceptance of the updated Privacy Policy.

---

## 9. Your Rights

Depending on your location (GDPR in EU, CCPA in California, etc.), you may have the following rights:

- **Right to Access:** You can access all your data directly within the app
- **Right to Rectification:** You can edit recording names and tags within the app
- **Right to Erasure:** You can delete recordings at any time
- **Right to Data Portability:** You can export recordings using the share function
- **Right to Object:** You can revoke permissions in iOS Settings

**Important:** All data is stored locally on your device. You have complete control 
and can exercise these rights directly through the app. When you export recordings 
via the Share function, exported files are subject to the privacy policies of the 
chosen destination service.

---

## 10. International Users

The App is designed to work globally. All data processing occurs locally on your device, regardless of your location. No data is transferred across borders or to external servers for processing.

---

## 11. Contact Information

If you have questions or concerns about this Privacy Policy or the App's data handling:

**Email:** jfalias [at] hotmail . de

(written with "[at]" deliberately to reduce automated harvesting; to reach us, replace "[at]" with "@" and remove the spaces.)

**Response Time:** Privacy inquiries are typically answered within 7 business days.

---

## 12. Legal Basis for Processing (GDPR)

For users in the European Economic Area (EEA) or United Kingdom, the legal basis for processing personal data is:

- **Consent:** You explicitly grant permission for microphone and location access
- **Legitimate Interest:** To provide core app functionality (recording with location tags)
- **Contract Performance:** To deliver the service you expect from the app

You can withdraw consent at any time by revoking permissions in iOS Settings or by uninstalling the app.

---

## 13. Data Security Measures

While all personal data is stored locally on your device, the following security practices are implemented:

- Audio files are stored in app's Documents directory (accessible via Files app, deleted on uninstall)
- iOS App Sandbox protects all data from other apps
- Database is protected by iOS sandboxing (not accessible without jailbreak)
- No personal data transmission (only map tiles are downloaded from Apple)
- Map tile downloads use standard HTTPS connections
- Device-level security (passcode, Face ID, Touch ID, device encryption) is recommended for additional protection

**Important:** When sharing recordings, be aware that GPS metadata is embedded in the file. The app shows a warning before sharing (v1.6.1+).

---

## 14. Summary

**What the App Collects:**
- Audio recordings (when you record)
- GPS coordinates (when you record)
- Recording metadata (timestamps, tags, etc.)
- GPS travel path (full GPS positions stored as rGPS metadata inside each M4A file)

**What the App Does NOT Do:**
- ❌ Send recording files to servers
- ❌ Send GPS coordinates to third-party servers
- ❌ Share personal data with third parties (except Apple MapKit for map display)
- ❌ Use analytics or tracking services
- ❌ Display advertisements
- ❌ Access your contacts, photos, or other files

**Your Control:**
- ✅ All data stays on your device
- ✅ Delete recordings anytime
- ✅ Revoke permissions anytime in iOS Settings
- ✅ Export your data via share function
- ✅ Complete data removal via uninstall
- ✅ GPS share warning alerts you before sharing recordings

---

**By using GPS Audio Recorder, you acknowledge that you have read and understood this Privacy Policy.**

---

## Document Version

- **Version:** 1.0 (iOS)
- **Last Updated:** April 27, 2026
- **Changelog:** Initial iOS-specific privacy policy based on Android v1.3

### Key Differences from Android Version

| Aspect | Android | iOS |
|--------|---------|-----|
| Storage Path | `/Android/data/com.gpsaudiorecorder/files/` | `/Documents/Recordings/` |
| Database | Room Database | SwiftData |
| Location Service | Google Play Services Location | Apple CoreLocation |
| Map Provider | OpenStreetMap (osmdroid) | Apple MapKit |
| Metadata Library | mp4parser | AVFoundation (native) |
| Share Mechanism | Android Intent | UIActivityViewController |
| Background Recording | Foreground Service + Notification | UIBackgroundModes (audio, location) |
| Permissions | Android Manifest permissions | Info.plist usage descriptions |

---

## App Store Privacy Labels (for reference)

When submitting to the App Store, the following privacy labels apply:

| Data Type | Collected? | Linked to User? | Used for Tracking? |
|-----------|------------|-----------------|---------------------|
| Audio Data | Yes | No | No |
| Location (Precise) | Yes | No | No |
| Usage Data | No | N/A | N/A |
| Diagnostics | No | N/A | N/A |
| Contact Info | No | N/A | N/A |
| Identifiers | No | N/A | N/A |

**Privacy Practices:** Data is not collected (all processing happens on-device), Data is not shared with third parties.
