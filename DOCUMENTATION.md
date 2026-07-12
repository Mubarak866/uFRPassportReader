# µFR Passport Reader - Documentation

## Table of Contents
1. [Application Overview](#application-overview)
2. [Reading Settings](#reading-settings)
3. [Upload Settings](#upload-settings)
4. [Data Privacy & Security](#data-privacy--security)
5. [Supported Devices](#supported-devices)
6. [Technical Specifications](#technical-specifications)
7. [Troubleshooting](#troubleshooting)

---

## Application Overview

### What is µFR Passport Reader?

µFR Passport Reader is a demonstration iOS application that enables users to:
- Read NFC chips embedded in e-Passports
- Verify the authenticity of Machine Readable Travel Documents (MRTD)
- Extract personal data using OCR technology
- Optionally extract photographs
- Upload data to a configured server

### How It Works

The application verifies NFC chip information in Machine Readable Travel Documents (MRTD) using:
- **OCR Technology**: Optically captured information from the document's Machine Readable Zone (MRZ)
- **Manual Entry**: Option to manually type MRZ data without scanning the document with your phone's camera

---

## Reading Settings

### 1. Read Personal Data
**Status**: Configurable (checkbox)
**Description**: Enables the app to read and extract personal information from the e-Passport's NFC chip
**Data Extracted**:
- Name
- Date of Birth
- Passport Number
- Nationality
- Gender
- Document Validity Dates

### 2. Extract Picture
**Status**: Configurable (checkbox)
**Description**: Extracts the photograph stored in the NFC chip
**Output**: Digital image file for verification purposes

### 3. Check Document Validity
**Status**: Configurable (checkbox)
**Description**: Verifies if the document is still valid and has not expired
**Checks**:
- Expiration date verification
- Digital signature validation
- NFC chip integrity

---

## Upload Settings

### Configuration
**Host URL**: `http://www.d-logic.com/nfc-rfid-reader-sdk/`

### Auto-Upload Feature
**Status**: Configurable (checkbox)
**Description**: When enabled, automatically sends extracted data to the configured host server after successful reading

**Important**: 
- This setting is optional
- Data transmission only occurs if explicitly enabled
- All data remains on the device if this option is disabled

---

## Data Privacy & Security

### Privacy Commitment

✅ **What the app does NOT do:**
- Does NOT collect personal information
- Does NOT store data on external servers (unless explicitly uploaded)
- Does NOT track user behavior
- Does NOT use analytics services
- Does NOT share data with third parties

✅ **What the app DOES do:**
- Keeps all data in device memory only
- Automatically deletes all data when app is closed
- Provides explicit control over data transmission
- Uses secure NFC communication protocols

### Data Lifecycle

```
1. NFC Read → Data loaded into device memory
2. User Review → Data displayed on screen
3. Optional Upload → Data sent to configured host (only if enabled)
4. App Close → All data automatically deleted from memory
```

---

## Supported Devices

### External NFC Reader
**µFR Nano Online**
- Wireless communication support
- Bluetooth communication support
- UDP and TCP/IP connections supported
- Future versions will add BLE support

### iPhone Requirements
- NFC capability (iPhone 7 and later)
- iOS compatibility with app version
- Proximity to NFC chip (typically <10cm)

### Connection Methods
- **Current**: UDP, TCP/IP, Bluetooth
- **Upcoming**: Bluetooth Low Energy (BLE)

---

## Technical Specifications

### OCR Technology
**Library**: Tesseract OCR for iOS (MIT License)
- High accuracy for MRZ zone reading
- Support for multiple languages
- Optimized for passport document format

### UI Framework
**Component**: DLRadioButton (MIT License)
- Radio button selection for settings
- Smooth user interface interactions

### Networking
**Library**: Alamofire (MIT License)
- HTTP/HTTPS communication
- Secure data transmission
- Configurable request/response handling

### In-App Purchases
**Library**: SwiftyStoreKit (MIT License)
- Handles app monetization
- Receipt validation
- Purchase management

---

## Troubleshooting

### Issue: NFC Reader Not Detected
**Solutions**:
1. Ensure NFC is enabled on your iPhone
2. Check device compatibility (iPhone 7+)
3. Verify external reader is powered on
4. Ensure Bluetooth/WiFi is enabled for wireless readers
5. Restart the application

### Issue: Unable to Read e-Passport
**Possible Causes**:
- NFC chip is damaged or not authentic
- Document has expired
- Interference from nearby devices
- MRZ data entered incorrectly

**Solutions**:
1. Verify passport is genuine
2. Check document validity dates
3. Minimize electromagnetic interference
4. Re-enter or re-scan MRZ data
5. Try different positioning relative to NFC reader

### Issue: Data Upload Fails
**Solutions**:
1. Check internet connectivity
2. Verify host URL is correct: `http://www.d-logic.com/nfc-rfid-reader-sdk/`
3. Ensure server is online and accessible
4. Check firewall/network restrictions
5. Review server logs for errors

### Issue: OCR Recognition Errors
**Solutions**:
1. Ensure good lighting when scanning MRZ
2. Hold camera steady during capture
3. Clean camera lens
4. Try manual MRZ entry instead
5. Check document is not damaged

---

## Additional Resources

- **Official SDK**: http://www.d-logic.com/nfc-rfid-reader-sdk/
- **NFC Forum Standards**: https://nfcpy.readthedocs.io/
- **ICAO MRTD Standards**: https://www.icao.int/

---

**Last Updated**: July 12, 2026
**Version**: 1.0
**Support**: Digital Logic (µFR Series)