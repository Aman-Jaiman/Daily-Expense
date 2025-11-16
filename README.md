# Modern Dark Expense Tracker 💳

A sleek, modern, and responsive dark-themed expense tracking application built with vanilla HTML, CSS, and JavaScript. Features glassmorphism design with neon accents, custom categories, and multi-currency support.

## ✨ Features

✅ **Dark Glassmorphism Design** - Modern UI with frosted glass effect and neon accents
✅ **Full-Screen Background Image** - Modern gradient background with blur effect
✅ **Custom Categories** - Create and save your own expense categories
✅ **Multi-Currency Support** - USD ($), INR (₹), EUR (€), GBP (£)
✅ **Neon-Accented UI** - Blue, purple, cyan, pink, and green neon colors
✅ **Smooth Animations** - Beautiful fade-in, slide-in, and hover animations
✅ **Responsive Design** - Works perfectly on desktop, tablet, and mobile
✅ **Add Expenses** - Quick add with amount, category, description, and auto-filled date
✅ **Edit Expenses** - Inline editing with save/cancel options
✅ **Delete Expenses** - Remove expenses with confirmation dialog
✅ **Total Calculation** - Automatic total expense calculation
✅ **Category Breakdown** - View spending by category in real-time
✅ **Persistent Storage** - All data saved to browser's localStorage
✅ **Modern Typography** - Poppins font for clean, professional look

## 🎨 Design Highlights

- **Color Scheme**: Dark theme with neon accents (blue, purple, cyan, pink, green)
- **Glass Effect**: Cards with 12px blur backdrop filter and semi-transparent backgrounds
- **Border Radius**: 16-20px rounded corners for modern look
- **Shadows**: Soft glowing shadows with neon color gradients
- **Typography**: Poppins font family for modern appearance
- **Background**: Dynamic gradient with subtle pattern and blur
- **Responsive**: Optimized for 480px (mobile), 768px (tablet), 1024px+ (desktop)

## 📁 Project Structure

```
Daily Expance/
├── index.html          # HTML structure with semantic layout
├── style.css           # Complete dark theme with glassmorphism
├── script.js           # Vanilla JavaScript with full functionality
└── README.md           # This file
```

## 🚀 Getting Started

### Requirements
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No server or dependencies needed

### Installation

1. Download or clone all files
2. Open `index.html` in your browser
3. Start tracking expenses!

### Using a Local Server (Optional)

**Python 3:**
```bash
python -m http.server 8000
# Visit: http://localhost:8000
```

**Node.js:**
```bash
npm install -g http-server
http-server
# Visit: http://localhost:8080
```

## 💡 How to Use

### Adding an Expense
1. Fill in the **Amount** field
2. Select a **Currency** (USD, INR, EUR, GBP)
3. Select a **Category** (or create a new one)
4. Enter a **Description**
5. Click **Add Expense** (date auto-fills today)

### Creating Custom Categories
1. Click the **+** button next to the Category dropdown
2. Enter a new category name (max 20 characters)
3. Click **Add** to save (or press Enter)
4. The new category is saved to localStorage and available for future use
5. Custom categories appear alongside default categories

### Viewing Expenses
- Expenses display in a modern card layout with currency symbol
- **Total Expenses** shows the sum of all spending
- **Category Breakdown** displays spending per category
- Most recent expenses appear first
- Currency symbol updates based on the first expense (or USD default)

### Editing an Expense
1. Click **Edit** on any expense
2. Inline form appears with all current values
3. Modify the fields (amount, currency, category, description, date)
4. Click **Save** to confirm or **Cancel** to discard

### Deleting an Expense
1. Click **Delete** on any expense
2. Confirm in the popup dialog
3. Expense is permanently removed

## 🎯 Technical Details

### HTML Structure
- Semantic HTML5 with proper form elements
- Background container with blur and overlay
- Glass card components
- Responsive grid layout
- Google Fonts integration (Poppins)

### CSS Features
- **CSS Variables** for consistent theming
- **CSS Grid** for responsive layout
- **Flexbox** for component alignment
- **Backdrop Filter** for glassmorphism effect
- **Linear & Radial Gradients** for backgrounds
- **Media Queries** for mobile responsiveness
- **Keyframe Animations** for smooth transitions
- **Neon Glowing Effects** with box-shadows

### JavaScript Architecture

**Core Functions:**

1. **Data Management**
   - `loadFromStorage()` - Load expenses from localStorage
   - `saveToStorage()` - Save expenses to localStorage
   - `loadCustomCategories()` - Load custom categories from localStorage
   - `saveCustomCategories()` - Save custom categories to localStorage

2. **Category Management**
   - `addCustomCategory(name)` - Add new custom category
   - `getAllCategories()` - Get all categories (default + custom)
   - `updateCategoryDropdown()` - Sync dropdown with all categories

3. **Expense Operations**
   - `addExpense()` - Add new expense with currency
   - `editExpense(id, updatedData)` - Update expense including currency
   - `deleteExpense(id)` - Remove expense
   - `startEdit(id)` - Show inline edit form
   - `saveEdit(id)` - Save edited expense
   - `cancelEdit()` - Close edit form

4. **Calculations**
   - `calculateTotal()` - Sum all expenses
   - `calculateCategoryTotals()` - Sum by category

5. **Rendering**
   - `renderExpenses()` - Display all expenses with currency symbols
   - `renderTotal()` - Update total display with currency
   - `renderCategoryBreakdown()` - Update category totals with currency

6. **Utilities & Events**
   - `generateId()` - Create unique IDs
   - `formatDate()` - Format dates for display
   - `setTodayDate()` - Auto-fill current date
   - `resetForm()` - Clear form
   - `escapeHtml()` - Prevent XSS attacks
   - `setupEventListeners()` - Setup custom category listeners

### Data Structure

```javascript
{
    id: "1731234567890-abc123def",
    amount: 25.50,
    currency: "USD",
    category: "Food",
    description: "Lunch at cafe",
    date: "2025-11-16"
}
```

### LocalStorage Keys
- **`expenseTrackerData`** - Stores all expense entries (JSON array)
- **`customCategories`** - Stores custom category names (JSON array)

## 🎨 Color Palette

| Element | Color | Hex |
|---------|-------|-----|
| Neon Blue | Primary accent | #00d4ff |
| Neon Purple | Secondary accent | #b000ff |
| Neon Cyan | Tertiary accent | #00ffff |
| Neon Pink | Danger/Delete | #ff006e |
| Neon Green | Success/Save | #39ff14 |
| Dark Background | Primary bg | #0a0e27 |
| Glass Card | Semi-transparent | rgba(20, 30, 60, 0.4) |

## 💱 Supported Currencies

| Currency | Symbol | Code |
|----------|--------|------|
| US Dollar | $ | USD |
| Indian Rupee | ₹ | INR |
| Euro | € | EUR |
| British Pound | £ | GBP |

Each expense stores its currency, and totals display with the appropriate symbol.

## 📱 Responsive Breakpoints

| Device | Size | Changes |
|--------|------|---------|
| Desktop | 1024px+ | 2-column layout |
| Tablet | 768px - 1023px | 1-column layout |
| Mobile | < 768px | Single column, optimized |
| Small Mobile | 480px | Larger touch targets |

## 🌐 Browser Compatibility

| Browser | Support |
|---------|---------|
| Chrome 90+ | ✅ Full support |
| Firefox 88+ | ✅ Full support |
| Safari 14+ | ✅ Full support |
| Edge 90+ | ✅ Full support |
| IE 11 | ❌ Not supported (uses modern CSS) |

## 🐛 Troubleshooting

**Q: Data not persisting?**
- A: Check if localStorage is enabled in browser settings
- In private/incognito mode, localStorage may be disabled

**Q: Styling looks off?**
- A: Ensure you're using a modern browser (Chrome 90+, Firefox 88+, Safari 14+)
- Clear browser cache and reload

**Q: Backdrop filter not visible?**
- A: This requires a modern browser. Try Chrome, Firefox, or Safari latest versions

**Q: How to clear all data?**
- A: Open browser console (F12) and run:
  ```javascript
  localStorage.removeItem('expenseTrackerData');
  location.reload();
  ```

## 🚀 Future Enhancements

- 📊 Charts and graphs (Chart.js integration)
- 🔍 Search and filter functionality
- 📤 Export to CSV/PDF with currency conversion
- 🌙 Light mode toggle
- 💾 Cloud sync with backend
- 🎯 Budget alerts and notifications
- 📈 Monthly/yearly analytics
- 🏷️ Delete custom categories
- 🔐 Password protection
- 📱 Progressive Web App (PWA)
- 🌍 More currency options

## 📝 Code Quality

- ✅ Well-commented code
- ✅ Clean function structure
- ✅ XSS protection with HTML escaping
- ✅ Form validation
- ✅ Error handling
- ✅ Semantic HTML
- ✅ Responsive CSS
- ✅ Vanilla JavaScript (no dependencies)

## 📄 License

Free to use for personal and commercial projects.
