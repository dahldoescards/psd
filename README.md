# Prospect Stats Dashboard

A web application for searching and exploring comprehensive prospect statistics across all seasons and levels.

## Features

- 🔍 **Fast Search**: Search by player name with fuzzy matching
- 📊 **Comprehensive Stats**: View all seasons and levels for each prospect
- 📱 **Responsive Design**: Works on desktop and mobile devices
- ⚡ **Client-Side**: No backend required, runs entirely in the browser

## Local Development

1. **Start a local server** (required due to CORS restrictions):
   ```bash
   # Python 3
   python3 -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   
   # Node.js (if you have http-server installed)
   npx http-server
   ```

2. **Open your browser** and navigate to:
   ```
   http://localhost:8000
   ```

## Deployment Options

### GitHub Pages (Recommended)

1. **Create a new repository** on GitHub
2. **Upload files**:
   - `index.html`
   - `Prospect stats.json`
   - `README.md`
3. **Enable GitHub Pages**:
   - Go to repository Settings → Pages
   - Select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click Save
4. **Access your site** at: `https://yourusername.github.io/your-repo-name`

### Netlify

1. **Drag and drop** the folder containing `index.html` and `Prospect stats.json` to [Netlify Drop](https://app.netlify.com/drop)
2. **Your site will be live** immediately with a random URL
3. **Customize the URL** in your site settings

### Vercel

1. **Install Vercel CLI**: `npm i -g vercel`
2. **Deploy**: `vercel --prod` in the project directory
3. **Follow the prompts** to set up your project

## File Structure

```
Prospect Dashboard/
├── index.html              # Main application file
├── Prospect stats.json     # Data file (your prospect statistics)
└── README.md              # This file
```

## Data Format

The application expects a JSON file with the following structure:

```json
[
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
        "Age": 22,
        "G": 50,
        "AVG": ".280",
        "HR": 15,
        "OPS": ".850",
        // ... other stats
      }
    ]
  }
]
```

## Browser Compatibility

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Performance Notes

- The application loads the entire JSON file into memory for fast searching
- For very large datasets (>50MB), consider implementing server-side search
- The search index is built client-side for optimal performance

## Customization

You can customize the application by modifying:

- **Styling**: Edit the CSS in the `<style>` section of `index.html`
- **Search behavior**: Modify the `searchPlayers()` method in the JavaScript
- **Displayed stats**: Update the `statsToShow` array in `renderSeasonStats()`
- **Layout**: Adjust the HTML structure and CSS grid layouts

## Troubleshooting

### "Failed to load JSON" Error
- Make sure you're running a local server (not opening the file directly)
- Check that `Prospect stats.json` is in the same directory as `index.html`
- Verify the JSON file is valid JSON format

### Search Not Working
- Ensure the JSON file has a `player` field for each prospect
- Check browser console for JavaScript errors
- Verify the data structure matches the expected format

### Performance Issues
- For large datasets, consider splitting the JSON by player or implementing pagination
- Use browser developer tools to monitor memory usage
- Consider implementing server-side search for datasets >100MB
