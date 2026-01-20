# dalgona-ar

A simple WebXR project using model-viewer to display animated 3D models in AR on Android and iOS devices.

## Features

- 🎨 **Cross-platform AR support**: GLB for Android/WebXR, USDZ for iOS
- 🎬 **Animated models**: Supports animated GLB files
- 📱 **Mobile-optimized**: Works seamlessly on Android and iOS devices
- 🖥️ **Desktop support**: Interactive 3D viewer for desktop browsers

## Setup

1. **Add your 3D models** to the `models/` folder:
   - `Dalgona-OneTake_0004.glb` - For Android devices and WebXR browsers
   - `Dalgona-OneTake_0004.usdz` - For iOS AR Quick Look

2. **Animation configuration**:
   - The animation track name is set to `animation_0` (already configured)

3. **Serve the files**:
   - You can use any local web server. For example:
     ```bash
     # Using Python 3
     python -m http.server 8000
     
     # Using Node.js (http-server)
     npx http-server -p 8000
     
     # Using PHP
     php -S localhost:8000
     ```

4. **Open in browser**:
   - Navigate to `http://localhost:8000` in your browser
   - On mobile devices, ensure you're accessing via HTTPS (required for WebXR)

## Usage

### Android Devices
- Click the "View in AR" button
- The model will open in ARCore Scene Viewer
- Place the model on a detected surface

### iOS Devices
- Click the "View in AR" button
- The model will open in AR Quick Look
- Use your device to place and view the model in AR

### Desktop Browsers
- Use mouse/trackpad to rotate and zoom the model
- The model will auto-rotate by default

## File Structure

```
dalgona-ar/
├── index.html          # Main HTML file with model-viewer
├── styles.css          # Styling for the page
├── models/             # Directory for 3D model files
│   ├── Dalgona-OneTake_0004.glb      # GLB file (Android/WebXR)
│   └── Dalgona-OneTake_0004.usdz     # USDZ file (iOS)
└── README.md          # This file
```

## Requirements

- Modern web browser with WebXR support (Chrome, Edge, Firefox)
- HTTPS connection (required for WebXR on mobile devices)
- For iOS: iOS 12+ with ARKit support
- For Android: Android 7.0+ with ARCore support

## Technologies Used

- [model-viewer](https://modelviewer.dev/) - Web component for displaying 3D models
- WebXR API - For AR experiences on supported browsers
- ARCore Scene Viewer - For Android AR experiences
- AR Quick Look - For iOS AR experiences

## Notes

- Model files: `Dalgona-OneTake_0004.glb` and `Dalgona-OneTake_0004.usdz`
- Animation track: `animation_0` (configured to autoplay)
- The `autoplay` attribute will automatically play the animation when the model loads
- For production, consider hosting on HTTPS-enabled servers

## License

MIT License - See LICENSE file for details
