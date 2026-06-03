Colour Hunter Architecture & System Documentation

This file details the low-level web platform APIs and algorithms that power the Colour Hunter game engine loop.

---

## 1. Hardware Video Stream Ingestion

* **API Link:** [`navigator.mediaDevices.getUserMedia()`](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia)
* **Core Application:** Prompts the user for video device permissions. It targets the rear primary camera asset array on mobile chassis units using the constraint `{ video: { facingMode: 'environment' } }`.
* **Pipe Execution:** Resolves to a native browser `MediaStream` object bound directly to the hardware camera source feed.

```javascript
video.srcObject = stream; // Pipes stream resource parameters to viewfinder display element