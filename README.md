# Aphaday

To use a custom logo image for the site, save your image file in the `icons` folder as `logo.png`. The application uses this file in the sidebar and login screen. For best results, make sure the image is square; the code will resize it to fit 16×16 or 40×40 pixels.

If you want the Progressive Web App icons (in `manifest.json`) to match the new logo, replace `icons/icon-192.png` and `icons/icon-512.png` with 192×192 and 512×512 versions of your logo. Keep the same filenames or update the manifest accordingly.

## Desktop application (offline)

The site can be wrapped into a simple desktop app using [Electron]. A minimal setup is already included:

1. install [Node.js] (which provides `npm`).
2. run `npm install` in the project root to fetch `electron` and `electron-packager`.
3. start the app during development with:
   ```bash
   npm run start
   ```
   This launches an Electron window that loads `index.html` locally; it does not require any network connection.
4. to build a self-contained Windows executable, run:
   ```bash
   npm run package
   ```
   The packaged application will be output under the `dist` folder. You can copy it to any offline PC and run it directly.

The configuration lives in `electron-main.js` (window size, menu, etc.) and can be customized.

[Electron]: https://www.electronjs.org/
[Node.js]: https://nodejs.org/
To preview the app, open `index.html` in a browser or run `Iniciar.ps1`/`Iniciar-App.bat` which starts a simple HTTP server and opens the page automatically.