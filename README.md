# Colour Hunter Prototype
A daily, web-based colour scavenger hunt game. Players use their smartphone to find real-world objects that match a target daily shade

## Current Milestone: Production-Ready MVP
This prototype implements a complete client-side game loop that matches real-world objects against a dynamic database without server overhead.

### Implemented Features:
1. **Asynchronous JSON Payload Ingestion:** Decouples game presentation layers from the data manifest. It fetches the color profile calendar out of an outboard `daily_colours.json` file.
2. **Epoch Modulo Scheduling Engine:** Tracks daily puzzle indexing using elapsed millisecond deltas calculated from a fixed target baseline epoch origin (`January 1, 2026`).
3. **Perceptually-Weighted Matching Formula:** Moves away from strict RGB linear math by utilizing a human eye perceptual distance model. It weights changes on the green wavelength heavily to simulate human optical variance.
4. **Adaptive UI Skins:** Calculates the raw luminance configuration of captured colors using the YIQ brightness scale, adjusting foreground font colors to stay readable over dark or bright targets.
5. **No-Jump Bounding Viewfinder:** Absolute layout alignment preserves viewport sizing. Toggling between live streaming and captured snapshot textures occurs seamlessly without layout shift.

### Tech Stack
- **HTML5 Canvas API**
- **Web MediaDevices API**
- **JavaScript Fetch API**
- **JSON Stroage Contexts**
- **CSS3 Transitions and Layout Engine**

## How to Run Locally

### Method 1: VS Code Live Server
1. Install the [**Live Server**](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension in VS Code.
2. Right-click `indext.html` and select **"Open with Live Server"**.

### Method 2: Python Terminal
If you have Python installed, open your terminal in this directory and run: 
```bash 
python -m http.server 8000