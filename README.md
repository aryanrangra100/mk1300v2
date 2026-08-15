# MK1300 V2 Keyboard Customizer - Web Version

This is the standalone web version of the **MK1300 V2 Keyboard Customization Software**. It runs directly in modern web browsers that support the standard **WebHID API** (such as Google Chrome, Microsoft Edge, and Opera).

## Features
- **Zero Install**: Configure your keyboard layout directly from your browser.
- **WebHID Connection**: Uses secure browser APIs to pair and customize your keyboard.
- **Identical Features**: Supports key mapping, macro configuration, RGB light edits, and firmware updates.

## How to Run Locally

### Prerequisites
- [Node.js](https://nodejs.org/) (includes `npm`)

### Steps
1. Navigate to the `web` directory in your terminal:
   ```bash
   cd web
   ```
2. Install the lightweight HTTP server dependency:
   ```bash
   npm install
   ```
3. Start the local server:
   ```bash
   npm run dev
   ```
4. Open your browser and navigate to:
   ```
   http://localhost:8080
   ```
5. Connect your keyboard:
   - Click the connection button on the UI (e.g., click on the device image).
   - When the browser displays the HID device request prompt, select your **MK1300 V2 Keyboard** and click **Connect**.

---

## How to Deploy to the Web

Since this is a fully static application, you can deploy it to any static web hosting provider in seconds:

### Option 1: Vercel / Netlify
1. Connect this folder or repository to Vercel/Netlify.
2. Set the build command to: *(leave empty)*
3. Set the output directory to: `.` (the root of the `web` directory)
4. Deploy!

### Option 2: GitHub Pages
1. Push the contents of the `web` directory to a GitHub repository.
2. Enable GitHub Pages in your repository settings and select the branch you want to serve.

---

## Chrome WebHID Permission Note
If the device doesn't pair or connect, make sure WebHID is enabled:
- In Chrome/Edge, verify that you see a USB/HID connection request dialog.
- Make sure no other application (like the desktop customizer app) is currently holding a connection lock on the keyboard.
