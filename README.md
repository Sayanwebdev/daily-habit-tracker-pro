# Daily Habit Tracker Pro

A modern, feature-rich habit tracking application built with HTML, CSS (Tailwind), and vanilla JavaScript.

## Features

- **Add & Manage Habits**: Create new habits with custom categories, goals, and descriptions
- **Daily Check-ins**: Mark habits as completed each day with visual feedback
- **Streak Tracking**: Automatically tracks your current streak for each habit with 🔥 indicators
- **Progress Analytics**: 
  - Real-time statistics showing total habits, today's progress, best streak, and weekly score
  - Interactive line chart displaying 7-day completion trends
- **Calendar View**: Visual calendar showing completion percentage for each day
- **Category Organization**: Automatic categorization of habits (Health, Productivity, Learning, Fitness, Mindfulness, Social, Other)
- **Data Persistence**: All data is stored in browser's localStorage
- **Data Management**:
  - Export habits and progress as JSON backup
  - Import previously exported data
  - Clear all data (with confirmation)
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices

## Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No installation or build process required

### How to Use

1. **Open the application**: Open `index.html` in your web browser
2. **Add a Habit**: Click the "Add Habit" button to create a new habit
   - Enter habit name
   - Select a category
   - Set daily/weekly goals
   - Add an optional description
3. **Track Daily**: Check off habits as you complete them each day
4. **Monitor Progress**: View real-time statistics and charts
5. **Manage Data**: Use Settings to export/import or clear data

## File Structure

```
daily habit tracker pro/
├── index.html       # Main application file (HTML, CSS, and JavaScript)
└── README.md        # This file
```

## Technologies Used

- **HTML5**: Semantic markup structure
- **Tailwind CSS**: Utility-first CSS framework via CDN
- **Chart.js**: Data visualization for progress trends
- **Vanilla JavaScript**: No frameworks; pure DOM manipulation
- **localStorage API**: Client-side data persistence

## Key Functions

### Data Management
- `loadData()` - Load habits and check-ins from localStorage
- `saveData()` - Save data to localStorage

### Rendering
- `renderHabits()` - Display today's habits list
- `renderCalendar()` - Display month calendar with completion indicators
- `updateStats()` - Update statistics dashboard
- `updateCategories()` - Update category summary

### Habit Operations
- `openHabitModal()` - Open add/edit habit dialog
- `saveHabit(event)` - Save new or edited habit
- `editHabit(habitId)` - Load habit into edit form
- `deleteHabit(habitId)` - Remove habit and related data
- `toggleHabit(habitId)` - Mark habit as completed/incomplete

### Analytics
- `calculateStreak(habitId)` - Calculate current streak for a habit
- `initProgressChart()` - Initialize Chart.js
- `updateProgressChart()` - Update 7-day completion chart

## Browser Compatibility

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## Tips

- **Backup Your Data**: Regularly export your data from Settings to ensure you don't lose progress
- **Best Streak**: Your best streak is calculated across all habits
- **Weekly Score**: Calculated as the average completion rate over the last 7 days
- **Calendar Colors**:
  - Green: 100% complete
  - Blue: 75%+ complete
  - Yellow: 50%+ complete
  - Orange: 1-49% complete
  - Gray: 0% complete

## Troubleshooting

### Add Habit button not working
1. Hard reload the browser: `Ctrl+F5` (Windows) or `Cmd+Shift+R` (Mac)
2. Check browser console for errors: `F12` → Console tab
3. Ensure JavaScript is enabled in your browser

### Data not saving
- Check if localStorage is enabled in your browser settings
- Try exporting your data before clearing browser data
- Import exported data after clearing

### Chart not displaying
- Ensure Chart.js CDN is accessible
- Check browser console for network errors

## Future Enhancements

- Weekly/monthly habit patterns
- Habit notes or journaling
- Custom notifications/reminders
- Dark mode theme
- Multi-device synchronization
- Social sharing features

## License

This project is open source and available for personal use.

## Support

For issues or suggestions, review your browser's developer console (F12) for error messages and ensure all CDN resources are loading correctly.
