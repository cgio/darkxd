# How  to Enable Adobe XD's Hidden Dark Theme

## Background

An official dark theme for Adobe XD does not currently exist. Since 2016, the feature request has garnered over [1,800 votes](https://adobexd.uservoice.com/forums/353007-adobe-xd-feature-requests/suggestions/12940362-dark-interface-overall-ui-including-side-panels). Adobe marked the request as "feature-in-the-backlog" in 2016.

On Windows, Adobe XD is a UWP app. Therefore, we can build on top of the "built-in" and unofficial dark theme. Read more about [UWP and colors here](https://docs.microsoft.com/en-us/windows/uwp/design/style/color). 

![Adobe XD Dark Theme](https://i.imgur.com/MzGZA4f.png)

## Compatibility

Tested with: 

* Adobe XD 19.2.22.3 for Windows downloaded via Creative Cloud
* Adobe XD 15.0.12.8 for Windows downloaded via Creative Cloud (old version, no longer supported)

## Requirements

* A decent text editor (i.e. Sublime Text or Notepad++)

## Instructions (Windows)

**At your own risk,** you can enable the dark theme via the following steps:

1. Because XD is installed as a Windows App (not a traditional desktop application), we need to enable access to XD's files within the `WindowsApps` folder (default path: `C:\Program Files\WindowsApps`). To enable access, we will use a registry modification (via a .reg file). The modification's author is Shawn Brink. You may download the modification from this page: https://www.tenforums.com/tutorials/3841-add-take-ownership-context-menu-windows-10-a.html
2. Follow Shawn's instructions. Double-click the appropriate .reg file to enable access and the "Take Ownership" right-click shell extension. 
3. Navigate to `C:\Program Files\WindowsApps`.  Find the folder that begins with `Adobe.CC.XD`. Inside, find the the `Themes` folder.
4. The themes folder should contain several files. One of those files should be `General.xaml`. Right-click `General.xaml` and click "Take Ownership." Next, make a backup (a copy) of `General.xaml` and store the backup elsewhere (i.e. a desktop or documents folder). *If you want to switch back to the light theme later, you will need to restore the original `General.xaml` file.*

5. Download the dark theme `General.xaml` [from this link](https://www.dropbox.com/s/yl06r2w6dah5to9/General.zip?dl=0). If needed, extract the `General.xaml` file.
6. Copy the "dark" `General.xaml` into XD's `Themes` folder, thereby replacing the original.

The dark theme should now be installed. You can now launch Adobe XD. Note that the first screen will be light. Beyond that, the XD interface will be dark. 

In creating the dark theme, I noticed that some areas were off-limits (e.g. the white slide out area surrounding the menu button, the color picker background, etc.).

*Remember to apply the restoration .reg file after you are content. Leaving the WindowsApps folder accessible reduces system security.*

## Notes

* If you want to edit `General.xaml` yourself, you can determine Adobe UI component hexadecimal colors by taking a screenshot and pasting the screenshot into XD or other capable image software. An eyedropper tool should show you the color code. Alternatively, an app like PicPick is effective.

* Be wary of Adobe's terms, although Adobe may want to avoid punishing users who seek better eye health.
