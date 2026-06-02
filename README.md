# Camera API Test
Prototype test for Colour Hunter

## Current Milestone: Camera API
Currently has a proof-of-concept showing that the browser can access a devices rear camera, render a video stream, and grab a frame from that video.

### Tech Stack
- **HTML5 Canvas API**
- **Web MediaDevices API**

## How to Run Locally

### Method 1: VS Code Live Server
1. Install the [**Live Server**](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension in VS Code.
2. Right-click `indext.html` and select **"Open with Live Server"**.

### Method 2: Python Terminal
If you have Python installed, open your terminal in this directory and run: 
```bash 
python -m http.server 8000
