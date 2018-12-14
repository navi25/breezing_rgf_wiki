* TypeError: fs.existSync is not a function
If you believe this is caused due to **"calling electron in renderer process by require('electron')"**, then change
require('electron) to window.require('electron'). As it could get confused by Browserify or Webpacks require's method signature.