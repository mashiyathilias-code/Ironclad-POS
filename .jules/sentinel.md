# Sentinel Security Journal

## 2024-05-22: Client-side Data Security and Brute-force Mitigation

### Learning:
- **Encrypted Backups:** In client-side only applications (IndexedDB), data exports are a major leak point. Implementing Web Crypto API (AES-GCM) with a user-defined Master PIN ensures zero-knowledge backups. This is critical for POS systems where transaction history is sensitive.
- **Brute-force on Static Pages:** Brute-force protection can be effectively implemented in pure JS using `localStorage` for lockout state. While bypassable by clearing site data, it provides a necessary friction layer for casual unauthorized access on shared devices.
- **CSP for POS:** POS systems should have strict CSP to prevent XSS from stealing session data or transaction details, especially when using `innerHTML` for dynamic UI components.

### Implementation Details:
- Added `encryptData` and `decryptData` using `SubtleCrypto`.
- Added `checkLockout` and `incrementFailedAttempts` to `loyalty.html` and `index.html`.
- Added `<meta http-equiv="Content-Security-Policy">` to restrict resources to `'self'`.
