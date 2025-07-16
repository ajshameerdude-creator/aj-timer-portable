const { app, BrowserWindow } = require('electron');
const path = require('path');

function createWindow() {
  const win = new BrowserWindow({
    width: 600,
    height: 400,
    webPreferences: {
      contextIsolation: true,
    },
  });

  win.loadFile(path.join(__dirname, '../build/index.html'));
}

app.whenReady().then(createWindow);
# aj-timer-portable
Portable React + Electron-based time counter
