# RunAsAdmin
Visual Studio extension to run Visual Studio as administrator

## Run Visual Studio as administrator
1. Install the extension
2. Restart Visual Studio
3. Visual Studio will be run as administrator

## Run Visual Studio as normal user
1. Go to Tools -> Options -> RunAsAdmin
2. Set Enabled to false
3. Restart Visual Studio

## Uninstalling the extension
When uninstalling the extension the current elevation mode will be preserved. If you have the extension Enabled in the options and uninstall it, Visual Studio will remain running as administrator. You have to use the RunAsAdmin options setting to enable or disable.

## Disabling the extension
When disabling the extension from within the Visual Studio extensions dialog nothing will happen like with uninstalling the extension. You have to use the RunAsAdmin options setting to enable or disable.

### Under the hood
The extension adds a registry entry at the following location: `HKEY_CURRENT_USER\Software\Microsoft\Windows NT\CurrentVersion\AppCompatFlags\Layers\`

Where the "Name" will be the path to Visual Studio and the value will be "RUNASADMIN" or "RUNASNORMAL"