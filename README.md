# FRC 2026 Scouting App 
Your scouting app folder should look like this:

```
scouting-app/
 - index.html           (main app file)
 - field-map.png        (field position)
 - background.png       (bg image)
```

## images

1. **field-map.png**
- field position map that shows up when you click "View Field Map"
- shows  the 5 starting positions (Depot Trench, Depot Bump, Middle, Outpost Bump, Outpost Trench)

2. **background.png**

## set up

1. **create a folder** (any name you like)

2. **add the HTML file** - Save index.html there folder

3. **add your images**:
   - save your field map as `field-map.png`
   - save your background image as `background.png`
   - put both in the same folder as `index.html`

4. **Open the app** - js double-click `index.html` twin (or open it in your tablet's browser)

## visual Modes

the app has 3 visual modes (cycle through them in settings):

1. **Standard Mode** - Clean white cards on green gradient background
2. **Glass Mode** - transparent frosted glass with the bg image

## Using on Tablets

### Android:
1. Open `index.html` in Chrome
2. Tap menu -> "Add to Home screen"

## to change image paths

If you want to use different filenames or put images in a subfolder, you can edit these lines at the top of the JavaScript in `index.html` :3 >.<

```javascript
const IMAGE_CONFIG = {
  fieldMap: './field-map.png',        // Change this path
  background: './background.png'       // Change this path
};
```

list of features

ahahaha... all missing data fields added (Push Into Outpost, Drove Over Bump, Intakes From)
qr code regeneration with history
clickable labels for easy selection
nandatory field indicators (*)
climb fields hide when Na
you can see the field map
UI (a waste of time tbh just make them run it through cmd prompt)
beautiful pear-themed UI
keeps scouter name on reset + it;ll increase match # by 1

## navigation buttons

The top navigation bar has buttons

- **⛶** (left) - toggle fullscreen 
- **↻** (middle) - regenerate previous QR codes
- **⚙** (right) - settings menu


current version: **2026.3.0**

