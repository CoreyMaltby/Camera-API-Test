# Colour Hunter Prototype
A daily, web-based colour scavenger hunt game. Players use their smartphone to find real-world objects that match a target daily shade

## Current Milestone: Data Decoupling and JSON Extraction
The prototype utilises an external payload schema to handle colour records.

### Implemented Features:
1. **Asynchronous JSON Ingestion:** Leverages native async/await `fetch()` calls to load global challenge profiles completely separate from core view markups.
2. **Epoch Modulo Progression:** Tracks daily progression using historical time-delta milliseconds offset against a baseline project epoch origin date (January 1, 2026).
3. **100-Shade Manifest:** Outboard `colors.json` database layer containing raw RGB, Hex, and tailored typographic designations.

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
