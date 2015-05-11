# Editor Framework

[Documentation](https://github.com/fireball-x/editor-framework/tree/master/docs) |
[Downloads](http://github.com/fireball-x/releases/) |
[Install](https://github.com/fireball-x/editor-framework#install) |
[Features](https://github.com/fireball-x/editor-framework#features)

The `Editor Framework` lets you easily write professional IDE like desktop tools just in HTML5 and
io.js.

The Framework is based on top of Electron and Polymer. It is heavily designed with the Electron's
main and renderer process architecture. To make multiple window communicate easily, `Editor Framework`
extends the Ipc API provided from Electron, make it easily to send and recieve callback amongs main
and renderers process.

It is designed for fully extends. In the core-level ( main process ), we doing this
by introduce a package management module and several register API. User can load or unload packages
lively without close or restart the app. In the page-level ( renderer process ), we use HTML5
Web-Component standards and includes the Polymer solution by default. User can extends the
widgets and panels, then refresh the page apply your changes.

## Install

```bash
# Install npm packages
npm install .

# Install bower packages
bower install .

# Install electron
gulp update-electron

# run the demo app
sh demo.sh
```

## Features

 - Package Management
   - Dynamically load and unload packages
   - Watch package changes and reload or notify changes immediately
   - Manage your packages in package manager Window
 - Panel Management
   - Freely docking panel in multiple window
   - Dynamically load user define panels from package
   - Easily register and respond ipc messages for your panel
   - Easily register shortcuts(hotkeys) for your panel
   - Save and load panels layout in json
   - Save and load panel profiles
 - Menu Extends
   - Dynamically add and remove menu item
   - Dynamically change menu item state ( enabled, checked, visible, ...)
   - Load user menu from packages
 - Commands
   - Register and customize commands for your App
   - A powerful command window (CmdP) for searching and executing your commands
 - Profiles
   - Allow user register different type of profile in demand ( global, local, project, ... )
   - Load and save profiles through unified API
 - Logs
   - Use Winston for low level logs
   - Log to file
   - A powerful console window for display and query your logs
 - Global Selection
   - Selection cached and synced amongs windows
   - User can register his own selection type
   - Automatically filter selections
 - Global Undo and Redo
 - Enhance the native Dialog
   - Remember dialog last edit position
 - Enhance Ipc Programming Experience
   - Lots of Ipc APIs for easily control ipc send and recv
   - Can sending ipc message to specific panel
   - Can sending ipc message to specific window
   - Add ipc callback, which can wait for a callback message
   - A powerfule ipc-debugger to help you writing better ipc programmes
