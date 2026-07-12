# µFR Passport Reader - Settings Guide

## Complete Settings Configuration Guide

### Navigation

In the app, tap the **Settings** icon to access all configuration options.

---

## READING SETTINGS

These settings control what data the app will attempt to read from the passport's NFC chip.

### 1. Read Personal Data ☐

**What It Does**:
Enables reading of personal information from the NFC chip, including:
- Full Name
- Date of Birth
- Gender
- Nationality
- Passport Number
- Document Issue Date
- Document Expiry Date
- Issuing Authority

**When to Enable**:
- ✅ When you need to extract personal information
- ✅ For identity verification purposes
- ✅ When you need complete passport data

**When to Disable**:
- ⚠️ If you only want to verify document validity
- ⚠️ If you're concerned about data exposure

**Default**: Unchecked (disabled)

---

### 2. Extract Picture ☐

**What It Does**:
Extracts and displays the photograph stored in the passport's NFC chip.

**Output**:
- Digital image file
- Can be saved or shared
- Used for facial verification

**When to Enable**:
- ✅ When you need the passport photo
- ✅ For biometric verification
- ✅ For identity confirmation

**When to Disable**:
- ⚠️ If you don't need the photo
- ⚠️ To minimize data extraction

**Default**: Unchecked (disabled)

---

### 3. Check Document Validity ☐

**What It Does**:
Performs validation checks on the passport, including:
- Expiration date verification
- Digital signature validation
- NFC chip integrity check
- Security feature verification

**Validation Checks**:
| Check | Description |
|-------|-------------|
| Expiry Date | Verifies document is not expired |
| Digital Signature | Confirms document authenticity |
| Chip Integrity | Ensures NFC data is not corrupted |
| Security Features | Validates security elements |

**When to Enable**:
- ✅ For authentication scenarios
- ✅ When document genuineness matters
- ✅ For official identity verification

**When to Disable**:
- ⚠️ For quick data reading only
- ⚠️ When validation is not required

**Default**: Unchecked (disabled)

**Important**: Enabling this setting may take longer to complete the read operation.

---

## UPLOAD SETTINGS

These settings control where and how data is transmitted from your device.

### Host Configuration

**Current Host URL**:
```
http://www.d-logic.com/nfc-rfid-reader-sdk/
```

**What It Is**:
The server address where data will be sent if auto-upload is enabled.

**How to Change**:
1. Tap on the Host URL field
2. Clear the current URL
3. Enter your server address
4. Tap "Confirm" to save

**Server Requirements**:
- Must be accessible via HTTP/HTTPS
- Must accept POST requests with JSON data
- Should implement proper data handling

**Important**: 
- Ensure you trust the destination server
- Use HTTPS when possible for security
- Verify server is online before enabling auto-upload

---

### 4. Send Data Automatically After Reading ☐

**What It Does**:
When enabled, automatically transmits extracted data to the configured host server immediately after successfully reading the passport.

**Data Transmitted**:
- Personal data (if "Read personal Data" is enabled)
- Passport photo (if "Extract Picture" is enabled)
- Validity check results (if "Check Document Validity" is enabled)
- Timestamp of reading
- Device identifier (optional)

**When to Enable**:
- ✅ For automated data collection workflows
- ✅ When you want hands-free operation
- ✅ For integration with backend systems

**When to Disable**:
- ⚠️ For privacy-conscious users
- ⚠️ When offline
- ⚠️ For local-only data processing

**Default**: Unchecked (disabled)

**Important Privacy Note**: 
Disabling this is the default for privacy reasons. Enable only if:
1. You understand where data is being sent
2. You trust the destination server
3. You have proper authorization
4. Applicable privacy regulations are followed

---

## WORKFLOW EXAMPLES

### Example 1: Simple Verification (Privacy Focused)

**Settings**:
- ☐ Read personal data - DISABLED
- ☐ Extract picture - DISABLED
- ☑ Check document validity - ENABLED
- ☐ Send data automatically - DISABLED

**Result**: Only verifies if passport is genuine and valid, no data extraction.

---

### Example 2: Complete Data Extraction (Local Only)

**Settings**:
- ☑ Read personal data - ENABLED
- ☑ Extract picture - ENABLED
- ☑ Check document validity - ENABLED
- ☐ Send data automatically - DISABLED

**Result**: Extracts all data and performs validation, data stays on device.

---

### Example 3: Automated Data Collection

**Settings**:
- ☑ Read personal data - ENABLED
- ☑ Extract picture - ENABLED
- ☑ Check document validity - ENABLED
- ☑ Send data automatically - ENABLED

**Result**: Complete extraction and automatic transmission to configured server.
⚠️ **Warning**: This requires proper authorization and privacy compliance.

---

### Example 4: Photo Verification Only

**Settings**:
- ☐ Read personal data - DISABLED
- ☑ Extract picture - ENABLED
- ☐ Check document validity - DISABLED
- ☐ Send data automatically - DISABLED

**Result**: Extracts and displays only the passport photo.

---

## BEST PRACTICES

### Security

✅ DO:
- Review all settings before reading a passport
- Understand what data will be extracted
- Trust the destination server if using auto-upload
- Use HTTPS for data transmission
- Keep app updated for security patches

❌ DON'T:
- Enable auto-upload without understanding consequences
- Use untrusted server URLs
- Send sensitive data over unsecured connections
- Leave app running with sensitive data displayed
- Share device with untrusted users

### Privacy

✅ DO:
- Disable unnecessary data extraction
- Keep auto-upload disabled unless needed
- Close app immediately after reading
- Review what data is being collected
- Use locally when possible

❌ DON'T:
- Transmit more data than necessary
- Assume all servers are secure
- Store unnecessary personal data
- Ignore privacy warnings
- Use without reviewing settings

### Performance

✅ DO:
- Enable validity checking only when needed
- Disable unnecessary features to speed up reading
- Ensure good connectivity before auto-upload
- Keep device battery charged
- Close other apps for better performance

---

## TROUBLESHOOTING SETTINGS

### Settings Not Saving
1. Tap "Confirm" button at bottom
2. Wait for confirmation message
3. Restart app if needed

### Can't Change Host URL
1. Ensure URL is valid format
2. Try copying/pasting instead of typing
3. Clear field completely before entering new URL

### Auto-Upload Not Working
1. Check internet connectivity
2. Verify host URL is correct and accessible
3. Ensure server is online
4. Check firewall/network restrictions
5. Review server logs for errors

### Settings Reverted After Closing App
- This is normal - data is not persisted
- Re-configure settings when reopening app
- Consider writing down your preferred settings

---

## RESETTING TO DEFAULT

**To reset all settings to defaults:**

1. Close the app completely
2. Restart the app
3. Go to Settings
4. All settings will be at default values

Default values:
- Read personal data: ☐ OFF
- Extract picture: ☐ OFF
- Check document validity: ☐ OFF
- Send data automatically: ☐ OFF
- Host: http://www.d-logic.com/nfc-rfid-reader-sdk/

---

**Need Help?**
Visit: http://www.d-logic.com/nfc-rfid-reader-sdk/

**Last Updated**: July 12, 2026
**Version**: 1.0