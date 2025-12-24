# IronClad Secure Retail Suite

A privacy-first, client-side retail management ecosystem consisting of a high-security Point of Sale (POS) and a dedicated Customer Loyalty management system. This suite is designed for businesses that prioritize data security and offline reliability using a "Zero-Knowledge" local vault architecture.

## 🛡️ Project Overview

The IronClad Retail Suite encrypts all sensitive business data—including inventory, financial logs, and customer details—using a Master PIN before storing it in the browser's persistent storage (IndexedDB/LocalStorage). No data is ever sent to a central server, ensuring total privacy.

### Core Components
* **IronClad POS (v2.3):** A full-featured sales terminal with inventory tracking, financial reporting (Z-Reports), and tax management.
* **IronClad Loyalty (v2.0):** A secure customer directory featuring tiered rewards, point redemption tracking, and digital loyalty card visuals.

## ✨ Key Features

### 🛒 Sales & Operations (`index.html`)
* **Encrypted Vault:** Secured by a 6-12 character Admin PIN that acts as the primary encryption key.
* **Dual-Role Access:** Separate permissions for "Admin" (full management) and "Cashier" (sales only).
* **Inventory Management:** Track sell price vs. unit cost to calculate net profit in real-time.
* **Financial Reporting:** Generate End-of-Day "Z-Reports" with detailed breakdowns of revenue, tax, and profit.
* **Print-Optimized Receipts:** Built-in CSS styles for clean physical receipt printing directly from the browser.

### 💎 Loyalty & Retention (`loyalty.html`)
* **Tiered Membership:** Customizable tiers (Bronze, Silver, Gold, Platinum, Black) that automatically update based on point thresholds.
* **Point Redemption Engine:** Configurable point-to-currency ratios for flexible reward programs.
* **Privacy-Focused Directory:** Customer phone numbers and emails are encrypted and stored locally.
* **Transaction History:** Granular logs for every point "Earn" or "Redeem" event.

## 🛠️ Tech Stack
* **Frontend:** HTML5, CSS3 (Modern Flex/Grid layout), Vanilla JavaScript.
* **Storage:** IndexedDB and LocalStorage for persistent, offline-first data.
* **Security:** Web Crypto API for client-side encryption.
* **Portability:** Single-file applications that run entirely in the browser without a backend server or database setup.

## 🚀 Getting Started

1.  **Deployment:** Simply download `index.html` and `loyalty.html`. You can open them directly in any modern web browser or host them on a static site provider (GitHub Pages, Netlify, etc.).
2.  **Initial Setup:**
    * On first launch, you will be prompted to create a **Master PIN**.
    * **Warning:** This PIN creates your encryption vault. If lost, the data cannot be recovered.
3.  **Data Portability:** Use the "Encrypted Backup" feature in the settings tab to export your data as a JSON file for migration or safe-keeping.

## ⚖️ License

This project is open-source and available under the **GNU General Public License v3.0 (GPLv3)**. 

---
*Developed with security and privacy as the core priority.*
