# Expense Tracker - Project Overview

## Project Description
A minimal, mobile-first expense tracking application for personal use between me and my wife. It’s designed for quick expense logging, hosted on GitHub Pages, and runs entirely in the browser with no server. Current live version: `https://bingeljell.github.io/expense-tracker/`.

## Core Features (As of March 31, 2025)
1. **Expense Entry**
   - Input amount (in ₹)
   - Category selection (dropdown with preset options: Uncategorized, Groceries, Dining, Utilities, Transport, Shopping, Other)
   - Optional notes
   - Automatic timestamp capture (stored as `YYYY-MM-DD HH:MM`, displayed as `DD Mon YYYY, H:MM AM/PM`)
2. **Expense Viewing**
   - Table display with columns: Amount (₹), Category, Date, Notes
   - Running total of all expenses
   - Totals by category
   - Sortable by date (toggle oldest/newest first)
3. **Data Management**
   - Clear all expenses with a confirmation button
   - Export expenses to CSV (columns: ID, Amount (₹), Category, Timestamp, Notes)

## Technical Stack
- **Frontend**: Plain HTML + JavaScript (single `index.html` with embedded JS)
- **Storage**: Local Storage (browser-based, persists until cache is cleared)
- **Styling**: Tailwind CSS via CDN (responsive, minimal setup)
- **Deployment**: GitHub Pages (static hosting, no server needed)

## Technical Requirements
- **UI/UX**: Mobile-first, single-page design; minimal, clean interface with improved spacing; easy one-handed operation; quick expense entry with a form.
- **Data**: Expense amount (number), category (string from dropdown), timestamp (auto-generated), notes (string, optional).

## Limitations
- Data is local to each device’s browser (no sync across devices).
- No authentication (public URL, but data isn’t shared).
- Clearing browser cache wipes all data.
- No monthly filtering in UI (CSV supports it via external tools).

## Future Ideas
- Monthly Filter: Add a dropdown or input to filter/export by month.
- UI Polish: Zebra stripes for table rows, fixed column widths, or color coding.
- Data Sync: Explore options for syncing between devices (e.g., manual import/export or a simple backend).
- Versioning: Use Git tags/branches for releases (to be explored later).



## Data Structure
```javascript
// Example expense object in Local Storage
{
  id: "123456789",           // Unique ID (timestamp-based)
  amount: 50.00,            // Number (in ₹)
  category: "Groceries",    // String (from dropdown)
  timestamp: "2025-03-28 16:44", // String (sortable, CSV-friendly)
  notes: "Milk and bread"   // String (optional)
}