# 📖 IronClad Secure Retail Suite: The Complete Guide

This guide covers everything you need to know to operate the **IronClad POS (v2.3)** and **IronClad Loyalty (v2.0)**. 

---

## 1. Core Security & Privacy
The IronClad suite is built on a **Zero-Knowledge** architecture. 
- **Encryption:** All data is encrypted using the AES-GCM standard via the Web Crypto API.
- **Ownership:** Your data never touches a cloud server. It lives in your browser's local database.
- **The Master PIN:** Your PIN is the encryption key. **If you lose this PIN, your data cannot be recovered by anyone.**

---

## 2. Getting Started
1. **Launch:** Open `index.html` (POS) or `loyalty.html` (Loyalty) in any modern browser (Chrome, Edge, Firefox).
2. **Initialization:** On your first visit, you will be prompted to set a **Master PIN**. 
3. **Login:** Every time you refresh or open the app, enter your PIN to decrypt the database.

---

## 3. IronClad POS (`index.html`)

### 🛒 Sales Terminal
* **Categories:** Use the top navigation pills to filter products.
* **Building an Order:** Click a product card to add it to the cart.
* **Quantity/Removal:** Use the `+` or `-` buttons in the cart to adjust quantities. Click the trash icon to remove an item.
* **Discounts:** Enter a percentage in the "Discount %" field to apply a price reduction to the entire subtotal.
* **Checkout:** 1. Enter the customer's phone or email (optional) to link to a loyalty account.
    2. Select a Payment Method (Cash, Card, etc.).
    3. Click **Charge Customer**.
    4. A **Printable Receipt** will appear. Use `Ctrl+P` (or `Cmd+P`) to print to a thermal or standard printer.

### 📦 Inventory & Management
* **Categories:** Create product categories first (e.g., "Beverages", "Electronics").
* **Products:** * **Unit Cost:** Enter what you paid for the item.
    * **Sell Price:** Enter the retail price. 
    * *Note: The system uses these two values to calculate your net profit.*
* **VAT/Tax:** Go to the **Management** tab to set your local tax percentage. This is applied automatically to every sale.

### 📈 Financial Reports
* **Dashboard:** View your Net Revenue, Total Tax Collected, and Net Profit in real-time.
* **Z-Reports:** Click "Generate Z-Report" to get a clean summary of the day's financial activity, broken down by payment method and product categories.

---

## 4. IronClad Loyalty (`loyalty.html`)

### 💎 Member Tiers
The system automatically upgrades customers based on their point balance:
- **Bronze:** Entry level.
- **Silver:** 500+ points.
- **Gold:** 2,000+ points.
- **Platinum:** 5,000+ points.
- **Black:** 10,000+ points (The highest tier).

### 👥 Managing Members
* **Registration:** Add a member with their name, phone, and email. These details are immediately encrypted.
* **Adjusting Points:** You can manually "Earn" or "Redeem" points.
    * *Earn:* For adding points based on purchases.
    * *Redeem:* For deducting points when a customer uses them for a discount.
* **History:** Every member has a granular log showing every transaction, the date, and the point change.

### ⚙️ Loyalty Configuration
In the **Config** tab, you can set:
- **Redemption Rate:** How much 1 point is worth in currency (e.g., 100 points = $1.00).
- **Earning Rate:** How many points a customer gets per currency unit spent (e.g., $1.00 = 10 points).

---

## 5. Maintenance & Backups

### 💾 Backing Up Data
Since data is stored locally in your browser, clearing your browser cache/history can delete your business data. 
1. Go to the **Settings/Management** tab.
2. Click **Export Encrypted Backup**.
3. Save the resulting `.json` file in a secure location (Cloud drive or USB).

### 📂 Importing Data
If you move to a new computer:
1. Open the app and log in with your PIN.
2. Go to the **Settings/Management** tab.
3. Click **Import Backup** and select your `.json` file.
4. The page will reload, and your data will be restored.

---

## 6. Access Control (POS Only)
In the Management tab, you can set a **Cashier PIN**:
- **Admin PIN:** Access to everything, including financial reports and price changes.
- **Cashier PIN:** Can only access the "Sales" and "History" tabs. They cannot see profit margins or delete inventory.

---

## ⚠️ Important Warnings
1. **Browser Privacy Mode:** Avoid using "Incognito" or "Private" mode, as browsers often delete local data as soon as the window is closed.
2. **Device Specific:** Data is **not** synced between your phone and your laptop unless you manually Export/Import the backup file.
