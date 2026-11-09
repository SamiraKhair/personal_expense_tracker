# Personal Expense Tracker

A simple web app for tracking daily income and expenses. Add transactions, review your history, see your totals, and check your remaining balance. Everything runs in the browser, and your data is saved on your device.

## Features

- **Dashboard** showing Total Income, Total Expenses, and Current Balance. The totals update automatically when a transaction is added or deleted.
- **Add Transaction** form with these fields:
  - Transaction Title
  - Amount
  - Transaction Type (Income or Expense)
  - Category (Food, Shopping, Transport, Bills, Entertainment, Salary, Other)
  - Date
- **Transaction History** table showing the title, amount, category, type, and date of each transaction, newest first.
- **Delete** any transaction from the history. The dashboard totals update right away.
- **Filters** to view All Transactions, only Income, or only Expenses. The dashboard totals always show the full picture, whatever filter is selected.
- **Data persistence** using the browser's localStorage. Transactions are still there after a refresh or when you reopen the browser.
- **Validation** on every field:
  - All fields are required.
  - Amounts must be numbers greater than 0, with up to 2 decimal places.
  - Dates must be valid and cannot be in the future.
  - Errors appear under each field.
- **Success message** for 3 seconds after a transaction is added.
- **Empty-state messages** when there are no transactions or none match the selected filter.
- **Responsive layout** for desktop, tablet, and mobile.

## Tech Stack

- HTML for structure
- [Tailwind CSS](https://tailwindcss.com) (via its CDN script) for styling
- Vanilla JavaScript for logic
- Browser localStorage for saving data

There are no frameworks, build steps, or packages to install.

## Project Structure

```
expense-tracker/
├── index.html   # The entire app: markup, Tailwind classes, and JavaScript
└── README.md    # This file
```

## How to Run

### Step 1: Clone the repository

```bash
git clone https://github.com/SamiraKhair/personal_expense_tracker.git
```


### Step 2: Open the app

Choose one of the options below.

**Option 1: Open the file directly (simplest)**

1. Double-click `index.html` in the cloned folder, or drag it into a browser window.

**Option 2: Serve it locally (optional)**

If you prefer to run it from a local server, open a terminal in the project folder and run one of these:

```bash
# Python 3
python -m http.server 8000

Then open `http://localhost:8000` in your browser.

**Note:** Tailwind CSS loads from its CDN, so you need an internet connection for the styling to appear.

## How to Use

1. **Add a transaction:** Fill in the title, amount, type, category, and date, then click **Add Transaction**.
2. **View your totals:** The dashboard at the top updates automatically.
3. **Filter the history:** Click **All Transactions**, **Income**, or **Expenses** above the table.
4. **Delete a transaction:** Click **Delete** on the row you want to remove.

## Data Storage

Transactions are saved in your browser's localStorage under the key `expense-tracker-transactions`. This means:

- Data stays on the device and in the browser where you added it.
- Data from one browser is not visible in another browser or on another device.
- Clearing your browser's site data will delete your transactions.

## Known Limitations

- Data is stored only in the current browser. There is no sync or backup.
- There is no editing of existing transactions; delete and re-add instead.
- Tailwind is loaded from its CDN, which is suited to development and prototyping rather than production.
