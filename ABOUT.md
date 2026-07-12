# About µFR Passport Reader

## Application Information

This demo app is used for **reading and verifying NFC chips in e-Passports** using either:
- External NFC Reader (µFR Series by Digital Logic), or
- Phone's built-in NFC chip

## How It Works

The application verifies the NFC chip in the **Machine Readable Travel Document (MRTD)** using optically captured (**OCR**) information from the document's **Machine Readable Zone (MRZ)**.

### Two Options for MRZ Data:
1. **Automatic**: Scan the document using your phone's camera - the app will use OCR to read the MRZ zone
2. **Manual**: Type in the MRZ data manually if you don't want to scan your document with your phone camera

## Key Features

✅ Read personal data from e-Passport NFC chip
✅ Extract embedded photograph
✅ Verify document authenticity and validity
✅ Optional automatic data upload
✅ Multiple connection methods (Bluetooth, UDP, TCP/IP)

## Privacy & Security

### Disclaimer
**This application is provided as-is and without any warranty.**

### Privacy Policy
**Application doesn't collect or store any personal information.**
- Data is kept only in device's memory
- Data is removed as soon as you close the app
- No external data collection or tracking
- No third-party data sharing

## Supported Devices

### Compatible External Readers
- **µFR Nano Online** - NFC Reader with Wireless and Bluetooth communication
- Connection types: BLE (coming soon), UDP, TCP/IP

### iPhone Requirements
- iPhone 7 or later (NFC capability required)
- Proximity reading range: ~10cm from NFC chip

## Technical Details

### Technologies Used

#### OCR (Optical Character Recognition)
- **Tesseract OCR for iOS** (MIT License)
- Enables automatic reading of Machine Readable Zone (MRZ)
- High accuracy for passport document format

#### User Interface
- **DLRadioButton** (MIT License)
- Smooth radio button selections for settings

#### Networking
- **Alamofire** (MIT License)
- Secure HTTP/HTTPS communication
- Data transmission to configured server

#### In-App Store
- **SwiftyStoreKit** (MIT License)
- Handles purchases and subscriptions

### Open Source Libraries

All open source libraries are licensed under MIT License:

1. **DLRadioButton**
   - Repository: https://github.com/DavydLiu/DLRadioButton
   - Purpose: UI radio button component

2. **Tesseract OCR for iOS**
   - Repository: https://github.com/gali8/Tesseract-OCR-iOS
   - Purpose: Optical character recognition for MRZ reading

3. **Alamofire**
   - Repository: https://github.com/Alamofire/Alamofire
   - Purpose: Networking and HTTP communication

4. **SwiftyStoreKit**
   - Repository: https://github.com/bizz84/SwiftyStoreKit
   - Purpose: In-app purchase management

## Roadmap

### Current Version (v1.0)
- ✅ NFC chip reading
- ✅ Personal data extraction
- ✅ Photo extraction
- ✅ Document validity checking
- ✅ OCR-based MRZ reading
- ✅ Manual MRZ entry
- ✅ Bluetooth connectivity
- ✅ UDP/TCP/IP support

### Upcoming Features
- 🔜 Bluetooth Low Energy (BLE) support
- 🔜 Enhanced security features
- 🔜 Multi-language support
- 🔜 Offline mode

## Common Questions

### Q: Is my data safe?
**A**: Yes. Your data never leaves your device unless you explicitly enable the upload feature, and even then it's only sent to the server you configure.

### Q: Can I use this with any passport?
**A**: Only e-Passports with NFC chips. Older passports without NFC cannot be read by this app.

### Q: Does the app work offline?
**A**: Yes, you can read and verify passports offline. Data upload to server requires internet connection.

### Q: What is MRZ?
**A**: Machine Readable Zone - the text at the bottom of passport's data page. It contains encoded information that can be read optically or manually entered.

### Q: How accurate is the OCR reading?
**A**: Tesseract OCR provides high accuracy for passport MRZ zones (typically >95%) when the document is clear and well-lit.

## Support & Feedback

For technical support, issues, or feature requests:
- Visit: http://www.d-logic.com/nfc-rfid-reader-sdk/
- Contact: Digital Logic Support

## License

MIT License - This application is open source and free to use.

---

**Version**: 1.0
**Release Date**: July 12, 2026
**Developer**: Digital Logic
**Platform**: iOS (iPhone 7+)