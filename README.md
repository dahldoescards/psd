# 🏟️ Prospect Stats Dashboard

A beautiful, fast web application for searching and exploring comprehensive prospect statistics across all seasons and levels.

## ✨ Features

- 🔍 **Smart Search**: Exact name matching with fuzzy fallback
- 📊 **Complete Stats**: All seasons and levels for each prospect
- 📱 **Responsive Design**: Works perfectly on desktop and mobile
- ⚡ **Lightning Fast**: Client-side search with no server required
- 🎨 **Beautiful UI**: Modern, professional design

## 🚀 Live Demo

**Your site will be live at**: https://dahldoescards.github.io/prospect-stats-dashboard

## 📁 Files

- `index.html` - The main web application
- `Prospect stats.json` - Your complete prospect data (6.5MB, 333K+ lines)
- `README.md` - This documentation

## 🔍 How to Use

1. **Search by exact name**: Type "Sheng-En Lin" → Shows only that player
2. **Search by partial name**: Type "Juan" → Shows all players with "Juan" in their name
3. **View all seasons**: Each player shows all their seasons sorted newest first
4. **See key stats**: Games, AVG, HR, RBI, OPS, ISO, wRC+, BB%, K%, SwStr%, pfxContact%, ERA, W-L, IP, FIP

## 📊 Stats Displayed

**Hitting Stats**: Games, AVG, HR, RBI, OPS, ISO, wRC+, BB%, K%, SwStr%, pfxContact%  
**Pitching Stats**: ERA, W, L, IP, K%, BB%, FIP

## 🎯 Search Behavior

- **Exact Match**: If you type the exact player name, only that player appears
- **Fuzzy Search**: If no exact match, shows all similar/partial matches
- **Real-time**: Search updates as you type (minimum 2 characters)

## 🌐 Deployment

### GitHub Pages (Current Setup)
- Repository: https://github.com/dahldoescards/prospect-stats-dashboard
- Live URL: https://dahldoescards.github.io/prospect-stats-dashboard
- Auto-deploys when you push changes

## 🎨 Customization

Edit `index.html` to customize:
- **Colors/Styling**: Modify the CSS variables
- **Stats Displayed**: Update the `statsToShow` array
- **Search Behavior**: Adjust the `searchPlayers()` method
- **Layout**: Change the grid and responsive breakpoints

## 📈 Data Structure

Your JSON contains prospect objects with:
```json
{
  "player": "Player Name",
  "oPlayerId": "unique_id", 
  "Height": "6'0\"",
  "Weight": 210,
  "Bats": "R",
  "Throws": "R", 
  "Age": 22,
  "llevel": "AAA",
  "stats": [
    {
      "Season": "2024",
      "Team": "Team Name",
      "llevel": "AAA",
      "G": 50,
      "AVG": ".280",
      "HR": 15,
      "OPS": ".850"
      // ... more stats
    }
  ]
}
```
