# 🎮 Game Hub Website

A modern, responsive game website built with pure HTML and CSS (no JavaScript required). Features theme switching, favorites, and a clean, modern design.

## Features

✨ **No JavaScript** - Pure HTML and CSS  
🎨 **Three Theme Options** - Light, Dark, and Auto (respects system preference)  
⭐ **Favorites System** - Mark games as favorites with checkboxes  
🎯 **Game Launch Options** - Open games in the same tab or new tab  
📱 **Fully Responsive** - Works on desktop, tablet, and mobile  
🚀 **Fast & Lightweight** - No dependencies, no build tools needed  

## Quick Start

1. Open `game-hub.html` in your browser
2. Use theme selector in header to switch between Light/Dark/Auto themes
3. Click the star button to add games to favorites
4. Click "Same Tab" or "New Tab" to launch games

## How It Works

### Theme Switching (Pure CSS)
Uses CSS `:has()` selector to detect radio button state - no JavaScript needed!

```css
body:has(.theme-label input[value="dark"]:checked) {
    /* Dark theme styles applied automatically */
}
```

### Favorites System
Simple checkbox inputs - styling applies when checked:

```css
.favorite-btn:has(input:checked) {
    background-color: var(--color-secondary);
    color: white;
}
```

### Game Launch Options
- **Same Tab**: Standard `<a>` link
- **New Tab**: Link with `target="_blank"` attribute

## Files Included

- **game-hub.html** - Main website with 6 sample games
- **styles.css** - Complete styling with CSS variables and theme logic
- **README.md** - This file

## Customization

### Add New Games

Edit `game-hub.html` and duplicate a game card, then update:

```html
<div class="game-card">
    <div class="game-image">
        <div class="placeholder-image">🎮</div>
    </div>
    <div class="game-info">
        <h3 class="game-title">Your Game Name</h3>
        <p class="game-description">Description</p>
        <div class="game-meta">
            <span class="game-tag">Category</span>
        </div>
        <div class="game-actions">
            <a href="path/to/game.html" class="btn btn-primary">Same Tab</a>
            <a href="path/to/game.html" target="_blank" class="btn btn-secondary">New Tab</a>
            <form class="favorite-form" method="post">
                <label class="favorite-btn">
                    <input type="checkbox" class="favorite-checkbox" />
                    ⭐ Add to Favorites
                </label>
            </form>
        </div>
    </div>
</div>
```

### Change Colors

Edit CSS variables in `styles.css`:

```css
:root {
    --color-primary: #6366f1;      /* Main brand color */
    --color-secondary: #ec4899;    /* Accent/favorites color */
    --color-background: #f8f9fa;   /* Light theme background */
    --color-surface: #ffffff;      /* Card surface */
    /* ... more variables */
}
```

### Create Games Folder

For organization, create a `games/` directory:

```
hub/
├── game-hub.html
├── styles.css
└── games/
    ├── tictactoe.html
    ├── dice.html
    └── memory.html
```

Then link to games: `href="games/tictactoe.html"`

## Browser Support

✅ Chrome/Edge 104+  
✅ Firefox 78+  
✅ Safari 15.4+  
✅ All modern mobile browsers  

**Requires**: CSS `:has()` selector support

## CSS Features Used

- **CSS Variables** - Dynamic theming
- **CSS Grid** - Responsive game layout
- **CSS `:has()` selector** - Form-state-based styling (no JS!)
- **CSS Media Queries** - Mobile responsiveness
- **CSS Gradients** - Visual effects

## Tips

1. **Replace emoji** - Use real game screenshots for the `.game-image` divs
2. **Add game folders** - Organize games in `games/` subdirectory
3. **Customize branding** - Change logo and colors in header
4. **Add transitions** - All elements have smooth 0.3s transitions built-in
5. **Mobile first** - Already responsive, no additional tweaks needed

## Example: Adding a Simple Game

1. Create `games/snake.html` with your game code
2. Add to `game-hub.html`:

```html
<div class="game-card">
    <div class="game-image">
        <div class="placeholder-image">🐍</div>
    </div>
    <div class="game-info">
        <h3 class="game-title">Snake Game</h3>
        <p class="game-description">Eat apples and grow longer!</p>
        <div class="game-meta">
            <span class="game-tag">Classic</span>
            <span class="game-tag">Arcade</span>
        </div>
        <div class="game-actions">
            <a href="games/snake.html" class="btn btn-primary">Same Tab</a>
            <a href="games/snake.html" target="_blank" class="btn btn-secondary">New Tab</a>
            <form class="favorite-form" method="post">
                <label class="favorite-btn">
                    <input type="checkbox" class="favorite-checkbox" />
                    ⭐ Add to Favorites
                </label>
            </form>
        </div>
    </div>
</div>
```

3. Done! Your game appears in the grid.

## License

Free to use and modify. Have fun! 🎮

---

Made with ❤️ by the Game Hub community
