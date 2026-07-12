# µFR Passport Reader

A demo iOS application for reading and verifying NFC chips in e-Passports using either external NFC Reader (µFR Series by Digital Logic) or the phone's native NFC chip.

## Overview

This application is designed to read and verify NFC chips embedded in Machine Readable Travel Documents (MRTD) such as electronic passports. The app uses optically captured (OCR) information from the document's Machine Readable Zone (MRZ) or allows manual data entry.

## Features

### Reading Settings
- ✅ Read personal data from NFC chip
- ✅ Extract picture from document
- ✅ Check document validity
- ✅ Support for both external NFC readers and phone's native NFC

### Data Handling
- **Privacy First**: Application doesn't collect or store any personal information
- **Local Storage Only**: Data is kept only in device's memory
- **Auto-Delete**: Data is removed as soon as you close the app

### Upload Settings
- Host: `http://www.d-logic.com/nfc-rfid-reader-sdk/`
- Optional automatic data transmission after reading

## Supported Devices

This app works with:
- **µFR Nano Online** - NFC Reader with Wireless and Bluetooth communication
- iPhone with NFC capability
- Future versions will include BLE, UDP, and TCP/IP support

## Technology Stack

### Open Source Libraries
- **DLRadioButton** - MIT License
  - https://github.com/DavydLiu/DLRadioButton
- **Tesseract OCR for iOS** - MIT License
  - https://github.com/gali8/Tesseract-OCR-iOS
- **Alamofire** - MIT License
  - https://github.com/Alamofire/Alamofire
- **SwiftyStoreKit** - MIT License
  - https://github.com/bizz84/SwiftyStoreKit

## Privacy Policy

This application is provided as-is and without any warranty.

**Data Privacy:**
- No personal data is collected by the application
- All data remains on the device's memory only
- Data is automatically deleted when the application is closed
- No data is transmitted unless explicitly configured by the user

## Disclaimer

This application is provided as-is and without any warranty. Use at your own risk.

## Getting Started

1. Launch the app on your iPhone
2. Configure reading settings (personal data, picture extraction, validity check)
3. Place your e-Passport near the NFC reader
4. The app will read and verify the NFC chip data
5. Review the extracted information
6. Optionally send data to configured host (if enabled)

## Requirements

- iOS device with NFC capability
- µFR Nano Online (external NFC reader) - optional
- e-Passport with NFC chip

## Contact & Support

For issues, questions, or support:
- Visit: http://www.d-logic.com/nfc-rfid-reader-sdk/
- Contact: Digital Logic

## License

MIT License - See LICENSE file for details

---

**Version:** 1.0
**Last Updated:** July 12, 2026