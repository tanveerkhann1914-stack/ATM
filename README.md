# 🏦 SBI ATM Simulator

An interactive, responsive, and visually stunning single-page ATM Simulator styled after State Bank of India (SBI) branding. Built entirely with Vanilla HTML5, CSS3, and JavaScript, it offers a realistic banking terminal experience directly inside the browser.

---

## 🌟 Key Features

*   **🔒 Secure PIN Authentication**: Enter the predefined security PIN to unlock the simulator (`default: 1234`).
*   **🕒 Real-Time Clock Widget**: Displays the current system date and time directly on the virtual screen.
*   **💾 Persistent Storage**: Utilizes the browser's `localStorage` API to save your balance and transaction history across browser sessions and reloads.
*   **💰 Cash Operations**:
    *   **Deposit Cash**: Instantly add funds with input validation.
    *   **Withdraw Cash**: Deduct funds with active overdraft protection (fails if balance is insufficient).
*   **📜 Mini Statement Generator**: Generates a standard thermal-style receipt showcasing your last 10 transactions.
*   **🖨️ Physical Receipt Printing**: Integrates standard browser printing mechanics (`window.print()`) for statements and receipts.
*   **🎨 Premium Glassmorphic UI**: High-fidelity ATM frame styled with smooth animations, neon terminal effects, and an animated gradient background.

---

## 🚀 How to Run Locally

Since this simulator runs entirely client-side, there is no setup or server required:

1.  **Clone or Download** this repository.
2.  Locate the [ATM1.html](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html) file in your file explorer.
3.  Double-click the file to open it in your preferred web browser (Chrome, Firefox, Safari, Edge, etc.).
4.  **Login Credentials**:
    *   **Default PIN**: `1234`
    *   **Starting Balance**: `₹50,000`

---

## 🛠️ Codebase Overview

The simulator logic and layout are contained entirely within [ATM1.html](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html). Below is a guide to the key functions and components:

### 🔑 Authentication & Navigation
*   [login()](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html#L307-L318): Handles verification of the entered user PIN against `1234`.
*   [showMenu()](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html#L329-L341): Constructs and mounts the primary ATM menu options on the display.
*   [logout()](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html#L515-L518): Refreshes the page to safely exit and lock the interface.

### 💳 Balance & Inquiry
*   [checkBalance()](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html#L344-L353): Shows current balance styled inside a high-visibility container.
*   [showHistory()](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html#L457-L484): Displays a complete log of all past transactions.

### 💵 Transactions & Receipts
*   [depositScreen()](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html#L356-L369) & [deposit()](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html#L372-L391): Processes user deposits and appends them to transaction history.
*   [withdrawScreen()](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html#L394-L407) & [withdrawMoney()](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html#L410-L434): Evaluates and updates the balance after performing a withdrawal.
*   [generateReceipt()](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html#L437-L454): Builds a formatted receipt slip with a printable layout.
*   [printMiniStatement()](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html#L487-L513): Outputs a statement with the last 10 transaction histories.

---

## 🎨 Visual Styles

The styling rules are specified within the `<style>` block in [ATM1.html](file:///c:/Users/husna/Desktop/ATM-11PM/ATM1.html#L9-L255):
*   **Animated Gradient Background**: A shifting linear-gradient creating a sleek dark ambiance.
*   **Glassmorphic Container**: Translucent ATM case using `backdrop-filter: blur()`.
*   **Neon Glow Screen**: A terminal style `#020813` dark canvas outline with `#06b6d4` box shadow.
