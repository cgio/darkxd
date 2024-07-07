# How  to Enable Adobe XD's Hidden Dark Theme

## Background

An official dark theme for Adobe XD does not currently exist. Since 2016, the feature request has garnered over [3,700 votes](https://adobexd.uservoice.com/forums/353007-adobe-xd-feature-requests/suggestions/12940362-dark-interface-overall-ui-including-side-panels). Adobe marked the request as "feature-in-the-backlog" in 2016.

On Windows, Adobe XD is a Universal Windows Platform (UWP) app. Therefore, we can build on top of the "built-in" and unofficial dark theme. Read more about [UWP and colors here](https://docs.microsoft.com/en-us/windows/uwp/design/style/color). 

![Adobe XD Dark Theme](https://i.imgur.com/TnBSihC.png)

## Compatibility

Tested with: 

* Adobe XD 57.1.12.2 for Windows downloaded via Creative Cloud
* Adobe XD 32.1.22.3 for Windows downloaded via Creative Cloud
	* Note: If you want to help, see if you can find the `General.xaml` color settings for: the line that appears under "Component" and related State rows (#E0F0FA), white dialog boxes, white instructional popups, the canvas area, etc.  Some of these UI components are entirely inaccessible via `General.xaml` modifications; i.e. .png image files such as `SP_Switch_Sm_D.scale-400.png`.
* Adobe XD 31.1.12.13 for Windows downloaded via Creative Cloud (old version; no longer supported)
* Adobe XD 27.0.12.7 for Windows downloaded via Creative Cloud (old version; no longer supported)
* Adobe XD 25.3.12.1 for Windows downloaded via Creative Cloud (old version; no longer supported)
* Adobe XD 19.2.22.3 for Windows downloaded via Creative Cloud (old version; no longer supported)
* Adobe XD 15.0.12.8 for Windows downloaded via Creative Cloud (old version; no longer supported)

## Requirements

* A compatible version of Adobe XD
* A decent Windows text editor (i.e. Sublime Text or Notepad++)

## Instructions (Windows)

**At your own risk,** you can enable the dark theme via the following steps:

1. Because XD is installed as a Windows App (not a traditional desktop application), we need to enable access to XD's files within the `WindowsApps` folder (default path: `C:\Program Files\WindowsApps`). To enable access, we will modify the Windows Registry via a .reg file. The .reg file's author is Shawn Brink. You may download the modification from this page: https://www.tenforums.com/tutorials/3841-add-take-ownership-context-menu-windows-10-a.html. Here is a direct link to the .reg file: https://www.tenforums.com/attachments/tutorials/247900d1568820808-add-take-ownership-context-menu-windows-10-a-add_take_ownership_to_context_menu.reg.
2. Follow Shawn's instructions. Double-click the appropriate .reg file to enable access and the "Take Ownership" right-click shell extension. 
3. Navigate to `C:\Program Files\WindowsApps`.  Find the folder that begins with `Adobe.CC.XD`. Inside, find the `Themes` folder.
4. The themes folder should contain several files. One of those files should be `General.xaml`. Right-click `General.xaml` and click "Take Ownership." Next, make a backup (a copy) of `General.xaml` and store the backup elsewhere (i.e. a Desktop or Documents folder). *If you want to switch back to the light theme later, you will need to restore the original `General.xaml` file.*
5. Download this project's unofficial dark theme `General.xaml` from https://www.dropbox.com/scl/fi/z4qmubbvmxo7owsafg3p6/General.zip?rlkey=h0othu23bcoxwgfsol67bd10z&st=ytud01s9&dl=0. If needed, extract the `General.xaml` file.
6. Copy the "dark" `General.xaml` into XD's `Themes` folder, thereby replacing the original.

The dark theme should now be applied. You can now launch Adobe XD. Note that the first screen will be light. Beyond that, a significant portion of the XD interface will be dark. 

*Remember to apply the restoration .reg file after you are content. Leaving the WindowsApps folder accessible reduces system security.*

## Notes

* If you want to edit `General.xaml` yourself, you can determine Adobe UI component hexadecimal colors by taking a screenshot and pasting the screenshot into XD or other capable image software. An eyedropper tool should show you the color code. Alternatively, an app like PicPick is effective.
* Be wary of Adobe's terms, although Adobe may want to avoid punishing users who seek better eye health.
* If a new version of XD is released, there is a decent chance the `General.xaml` will need an update. The modified `General.xaml` included here may not work and cause XD to crash. If you want to work on creating a dark theme for the new `General.xaml`, diff the `General.xaml` included here with the new `General.xaml`, analyze/compare and carefully make the appropriate changes to the new `General.xaml`. Test periodically for crashes/instability by placing the updated `General.xaml` in the `Themes` folder.
