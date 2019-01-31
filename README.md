# How  to Enable Adobe XD's Hidden Dark Theme

## Background

An official dark theme for Adobe XD does not currently exist. Since 2016, the feature request has garnered over [1,300 votes](https://adobexd.uservoice.com/forums/353007-adobe-xd-feature-requests/suggestions/12940362-dark-interface-overall-ui-including-side-panels). Adobe has marked the request as "feature-in-the-backlog."

I pay for a couple of Adobe services. I received an unexpected email from Adobe indicating that I received a one-year license to XD. I decided to try it out. I was disappointed with XD's dark mode omission. Arguably, Sketch (Mac only) is XD's biggest competitor. Sketch has a dark mode. Many of Adobe's other design products do, too. Less light, less eye strain. Fortunately, within a short period of time, I discovered that a hidden dark theme exists and is relatively easy to unlock.

## Compatibility

Tested with: 

* Adobe XD 15.0.12.8 downloaded via Creative Cloud

## Requirements

* A decent text editor, such as Sublime Text or Notepad++

## Instructions

**At your own risk,** you can enable the dark theme via the following steps​:​

1. Note that XD is installed as a Windows App; not a traditional desktop application. Special access is needed for working with XD files within the `WindowsApps` folder (default path: `C:\Program Files\WindowsApps`). To enable access, we will use a registry modification (via a .reg file). The modification's author is Shawn Brink. You may download the modification from this page: https://www.tenforums.com/tutorials/3841-add-take-ownership-context-menu-windows-10-a.html
2. Refer to Shawn's instructions. Double-click the appropriate .reg file to enable `WindowsApps` access. Note that a separate .reg file restores prior settings. You can use that file later once all the steps are done.
3. Assuming you now have access to WindowsApps and the directory's subfolders, navigate to the folder that begins with `Adobe.CC.XD`. Navigate one step further into the Themes folder.
4. The themes folder should contain several files. My folder contains the following: 
   * `General.xaml`
   * `SpectrumBrushes.xaml`
   * `SpectrumTheme.xaml`
   * `SpectrumThemeDark.xaml`
   * `SpectrumThemeLight.xaml`

5. Make backups (copies) of all the .xaml files and store them elsewhere, i.e. a desktop or documents folder. You may need to restore the originals later if XD fails to load or your experiments have gone too far.
6. In the separate folder where your copies are stored, make copies of the copies. You will be editing the `General.xaml `file, so make sure the file you are editing is `General.xaml` (and not `General - Copy.xaml`) from within your personal folder (not a WindowsApps folder). Later, you will be replacing the WindowsApps `General.xaml` with modified `General.xaml` from your personal folder.
7. Make sure XD is closed. Using your text editor, open the General.xml from your personal folder. As you will see, General.xaml is quite legible, as it is a Microsoft  XML-based language. General.xaml contains an "ADOBE CONFIDENTIAL" notice. Therefore, I have written the remaining instructions accordingly, so pay attention closely. I have to walk the line.
8. In theory, it would make sense if Adobe constructed separate definitions for light and dark themes within the `General.xaml` file. What would happen if you, for educational purposes, switched the text `"Light"` to `"Dark"` and `"Dark"` to `"Light"`? What would happen if you saved the file? What would happen if you replaced the `General.xaml` in the XD's `Themes` folder with the one you modified? Would Adobe XD have the hidden dark mode enabled?
9. Remember to apply the restoration .reg file after you are content. Leaving the WindowsApps folder accessible reduces security.

If necessary, revert changes by following the theory in step eight backwards. 

## Notes

* There are likely other ways to do this and the themes can further be expanded upon, so feel free to experiment. Do not expect the dark mode to apply everywhere. I did all of this all a bit quickly and I am reasonably satisfied with the results. Menu text color may need some adjustments to improve legibility. Use common sense to figure that out.

* You can figure out the hexadecimal color of Adobe UI components by taking a screenshot and pasting the screenshot into XD or other capable image software. An eyedropper tool may show you the hex color code. PicPick's Color Picker also works. The hex format Adobe uses is relatively self-explanatory. Hint: remember that graphic/web design often involves a hex alpha value in addition to hex color values.

* Be wary of Adobe and the confidentiality terms, though it would look bad upon Adobe for pursuing users who want better eye health. Also, Adobe is looking to increase user adoption, as per the email one-year XD access promotion I received.
