# Expense Tracker - Project Overview

## Project Description
A super-minimal, mobile-first expense tracking application for personal use between two users (me and my wife). It’s designed for quick expense logging with a simple interface, hosted on GitHub Pages, and runs entirely in the browser.

## Core Features
1. **Expense Entry**
   - Input amount
   - Category selection (dropdown with preset options)
   - Optional notes
   - Automatic timestamp capture
2. **Expense Viewing**
   - List all expenses chronologically
   - Display amount, category, timestamp, and notes (if provided)
   - Running total of all expenses
   - Totals by category
3. **Data Management**
   - Clear all expenses with a button
   - Export expenses to CSV for review
4. **Future Enhancements (Later Phases)**
   - Filter/sort by category
   - Filter by month for export

## Technical Requirements

### UI/UX Requirements
- Mobile-first, single-page design
- Minimal, clean interface with improved spacing
- Easy one-handed operation
- Quick expense entry with a form

### Data Requirements
- Expense amount (number)
- Category (string, selected from dropdown)
- Timestamp (auto-generated)
- Notes (string, optional)

## Technical Stack

### Frontend
- **Plain HTML + JavaScript**
  - Single `index.html` file with embedded JS
  - No frameworks, no build tools
  - Runs entirely in the browser
- **Local Storage**
  - Simple key-value storage in the browser
  - Persistent across sessions
  - Sufficient for small-scale personal use
- **Tailwind CSS (via CDN)**
  - Rapid, responsive styling
  - No setup required—just a script tag

### Authentication
- None currently
- Optional: Simple JS-based password prompt (not secure, but fine for personal use)

### Deployment
- **GitHub Pages**
  - Free static hosting
  - Accessible from any device (live at https://bingeljell.github.io/expense-tracker/)
- **GitHub Actions** (optional)
  - Automate deployment if desired

## Data Structure
```javascript
// Example expense object stored in Local Storage
{
  id: "123456789",         // Unique ID (timestamp-based)
  amount: 12.50,          // Number
  category: "Groceries",  // String (from dropdown)
  timestamp: "3/28/2025, 10:30 AM", // String from Date.toLocaleString()
  notes: "Milk and bread" // String (optional)
}