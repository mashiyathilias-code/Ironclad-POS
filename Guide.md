# 🛡️ IronClad POS & Loyalty: Complete User Guide

This guide covers the operation of the **IronClad POS Terminal** and the **IronClad Loyalty Vault**. These tools are designed to be "Zero-Knowledge" systems—meaning your data is encrypted locally in your browser using **AES-GCM 256-bit encryption**. No data is ever sent to a server.

---

## 🗝️ Core Security Concepts

### 1. The Master PIN
Upon first launch, you will create an **Admin PIN**. This PIN is the "key" to your database.
*   **⚠️ Warning:** If you forget this PIN, your data cannot be recovered. 
*   **Lockout:** Entering the wrong PIN 3 times will trigger a 30-second security lockout.

### 2. Browser Storage
Data is stored in your browser's **IndexedDB**. 
*   **Clearing Cache:** If you "Clear Site Data" or "Reset Browser Settings," your database will be deleted. 
*   **Persistence:** Always click **"Allow"** if your browser asks for permission to persist storage.

---

## 🛒 Module 1: IronClad POS (Sales & Inventory)

### 1. Initial Configuration
Before making your first sale, navigate to the **Looks & Users** tab:
*   **Categories:** Create groupings (e.g., "Food", "Apparel") to organize your terminal.
*   **Payment Methods:** Add methods like "Cash," "Credit Card," or "Crypto."
*   **Tax & Loyalty:** Set your global VAT % and the Loyalty Earn Rate (points per $1 spent).
*   **Cashier Mode:** Set a "Cashier PIN." This allows staff to make sales without seeing financial reports or inventory settings.

### 2. Managing Inventory
Navigate to the **Inventory** tab:
*   **Adding Items:** Enter the name, sell price, unit cost, and current stock.
*   **Stock Tracking:** The system automatically deducts stock when a sale is made and restores it if a transaction is voided.

### 3. Sales Terminal Workflow
1.  **Selection:** Click product cards or use the **Search Bar** (top) to add items.
2.  **Barcode Scanning:** Focus the search bar and scan a barcode. If the ID matches a product, it adds to the cart automatically.
3.  **Customer Tagging:** Enter the customer's phone or email in the "Customer" field. This is used to track points in the Loyalty module.
4.  **Discounts:** Apply a percentage discount if applicable.
5.  **Checkout:** Select the payment method and click **Charge Customer**. A secure receipt will be generated.

### 4. Voids & Financials
*   **History:** View past sales in the **History & Void** tab. Click **Void** to undo a sale, which generates a balancing negative transaction and returns items to stock.
*   **Z-Report:** At the end of a shift, go to **Financials** and click **End-of-Day Z-Report**. This provides a print-ready summary of sales, taxes, and payment method breakdowns.

---

## 💎 Module 2: Loyalty Vault (Customer CRM)

### 1. Setting Tiers & Values
Navigate to the **Settings** tab to define your program:
*   **Point Value:** Define the cash value of 1 point (e.g., `0.01` means 100 points = $1.00).
*   **Custom Tiers:** Create tiers like "Silver," "Gold," and "Platinum." Set the minimum points required for each. The "Card Visual" in the directory will change color based on the tier's gradient.

### 2. Member Management
*   **Adding Members:** Use the **+ New Member** button. Use a unique identifier (like a phone number) as their ID.
*   **Member Directory:** Search for customers to see their digital "Loyalty Card," current point balance, and transaction history.

### 3. Points Workflow
*   **Adding Points:** Click **Add Points** when a customer makes a purchase. 
*   **Redemption:** Click **Redeem**. The system will calculate the cash value of the points based on your settings and deduct them from the member's balance.

---

## 💾 Data Maintenance (Backups)

Since data is stored only in your browser, **regular backups are mandatory**.

1.  **Exporting:** Both modules have an **Export** button in their respective settings/management tabs. This downloads a `.json` file containing your entire database.
2.  **Importing:** To move to a new computer or restore data, click **Import** and select your latest backup file.
3.  **Recommendation:** Export a backup daily after your Z-Report and save it to a secure cloud drive or USB stick.

---

## 🛠️ Troubleshooting
*   **Search not working?** Ensure your items have the correct Category assigned.
*   **Printer formatting?** When printing receipts or Z-Reports, enable "Background Graphics" in your browser's print settings to ensure colors and lines appear correctly.
*   **Locked out?** Wait the full 30 seconds for the timer to clear before attempting your PIN again.
