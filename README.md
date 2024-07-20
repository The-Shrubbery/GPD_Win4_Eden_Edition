# GPD Win4 Eden Edition
Improve FPS, temps, and battery life on your GPD Win4!

## Setup Guide for GPD Win4, updated in July 2024

![image](https://www.gizmochina.com/wp-content/uploads/2022/09/GPD-Win-4-White-Silver-1.png)

<!-- GETTING STARTED -->
## Getting Started

If performance on your Win4 is not as expected, this guide will hopefully help resolve your issues and provide some useful tips on using the powerful softwares available for our amazing handheld.</br>
</br>
The softwares referenced in this guide are:</br>
[**Rivatuner Statistics Server**](https://www.guru3d.com/download/rtss-rivatuner-statistics-server-download/)</br>
[**Motion Assistant**](https://drive.google.com/file/d/1X4CrqWz2VKiyHlwPI32oQrqUarWi6jTG/view?usp=sharing)</br>
[**Auto TDP**](https://cdn.discordapp.com/attachments/993089115245514783/1239066546022776922/TDP-399.zip?ex=669be0e5&is=669a8f65&hm=dfbf1538e1a3291df0ee27ebdb37882fa490999289205710b03746774b262182&)</br>
[**Handheld Companion** ](https://github.com/Valkirie/HandheldCompanion/releases)</br>
Optional:</br>
[**Winaero Tweaker**](https://winaero.com/downloads/winaerotweaker.zip)</br>
[**Revo Uninstaller**](https://download.revouninstaller.com/download/RevoUninstaller_Portable.zip)</br></br>


As we proceed through the guide we will be installing and configuring each of these softwares in order.</br>
If any of these are already installed on your system, please make sure they are all up to date!</br></br>

![image](https://www.notebookcheck.com/fileadmin/Notebooks/News/_nc3/gpdwin3.JPG)

### Rivatuner Statistics Server

Rivatuner, or RTSS, is a commonly used frametiming software.  It basically does the same thing as Vsync, but is effective across the whole system.  Other applications in this guide require the software for full functionality, and it requires minimal setup!</br></br>

Simply [download](https://www.guru3d.com/download/rtss-rivatuner-statistics-server-download/) and install the software, reboot once it has finished installing.</br>
Once you are back online, open RTSS and in the main window select `Start with Windows` to switch it `ON`.  In the `Framerate Limit` box, click and type `60`, then hit `Enter`.</br>
Your RTSS should be set up and can be safely **minimized** to the background.</br></br>
![image](https://static.wikia.nocookie.net/onexplayer/images/f/f3/Rtss.png/revision/latest/scale-to-width-down/1200?cb=20220109212504)


### Motion Assistant

Motion Assistant is the official GPD software, it has firmware control over some of the functions on your Win system, and ideally is installed **but not running in the background!** </br>  
In fact, Motion Assistant should not be running at all in order to get best performance.  This is a "set-and-forget" configuration! </br></br>

Firstly we must install / update the software from [the GPD Google Drive](https://drive.google.com/file/d/1X4CrqWz2VKiyHlwPI32oQrqUarWi6jTG/view?usp=sharing).</br>
Once the software is installed, open it and navigate to the TDP tab.  This is where we will do most of our work, configuring emulated controllers and hotkeys will be covered later in the guide using a different software.</br>
Set your software to the settings shown here:</br>
![image](https://cdn.discordapp.com/attachments/950574522011119707/1263975178719854734/image.png?ex=669c301e&is=669ade9e&hm=51db297ab5bc1313391ede8c9342986abb0c28ee3fa831d5f4c15ff875d23c59&) </br></br>

Check and uncheck the `Auto Lock GPU`, `Optimize GPU`, and `Custom Float GPU` to be sure the options are set correctly.  Fill out empty fields or input the value again and hit `Enter` to ensure everything is set.</br>
Next, click the `Unlock GPU` button and press `OK` on the dialogue box to hibernate your system.  Wait for it to turn off, then bring it back from hibernate.</br>
Ensure `Start with windows` is **UN-checked** to prevent Motion Assistant from interfering in further steps.</br>
Your Motion Assistant should be set up!  Close Motion Assistant and make sure it is not minimized or running in your Task Tray.</br></br>

Note:</br>
If your `FPS Limit` text is greyed out, install [**RTSS**](https://www.guru3d.com/download/rtss-rivatuner-statistics-server-download/) as mentioned previously.  Be sure you have **rebooted** after the installing Motion Assistant.</br></br>

### AutoTDP

Ciphray's AutoTDP.bat file is a custom made utility that does some obscure magic that makes Windows perform twice as well.  Cannot thank you enough, Ciphray.</br>
Thankfully, installing is extremely easy: extract the .zip file to a folder of your choice (I have a folder in My Documents called TDP) and run `TDP_UV_MENU_FAST.bat`.</br>
![image](https://media.discordapp.net/attachments/1069768559699431525/1264031170170196078/image.png?ex=669c6443&is=669b12c3&hm=d1d30e9c168ce3173639915cd46dede97d0312340b0729188522a7c3d6510d2a&=&format=webp&quality=lossless&width=932&height=524)
If your settings look different than the screenshot, do not mind it at all.  In the next section we will configure all that.  Check back after finishing the guide and see your changes reflected in the TDP Menu!</br></br>

From the TDP Menu do the following key combinations on your Win4: </br>
`R -> 0` to open advanced Windows settings and disable Superfetch.  Once that refreshes, press `M -> 1` and wait for refresh.  Press `3` and `4` as well, waiting for the menu to refresh between presses.  Now press `Q` twice to get back to the main menu.</br>
`S -> I -> E` to prevent Windows from giving all your power to the CPU instead of GPU.  Make sure the `Cycle Power Scheme Currently` value is set to `Power Saver-EPP` by pressing the `F` key as needed.  Press `Q` to return to the main menu.</br>
`Y -> 7` to open the AC/DC power menu.  Press `1`, `2`, and `3` as needed so each value is set to `Max Performance`, then press `A` to save settings.</br></br>

Once you are back to the main menu, press `Q` to exit without selecting a TDP.  All settings will persist through reboots and are effective even if TDP is not running.  AutoTDP is now configured on your Win4!</br></br>

### Handheld Companion

Handheld Companion controls system performance, emulated controllers, and performance overlay.  This app is where you do all TDP and fan curve customization, and supports per-applicaiton profiles.</br>
Firstly after installing the software and rebooting, open Handheld Companion and make sure your emulated controller is behaving correctly and not showing multiple inputs.</br>
Next, go in to the `Device` tab and enable the `Controllable power (cTDP) override`.  Set the values to `5` for min and `35` for max.</br>
The `Performance` tab has all the action.  Here are a pair of screenshots of the performance tab, configure your system to follow these settings:
![image](https://github.com/user-attachments/assets/a67d0d72-b1b3-4f4b-9986-9a1b4e9e2e08)</br>
Your TDP should adjust by itself thanks to AutoTDP, however if you are getting low CPU/GPU usage try to toggle the `Automatic TDP` setting to `60fps`.</br>
![image](https://media.discordapp.net/attachments/950574522011119707/1263947378784993404/image.png?ex=669c163a&is=669ac4ba&hm=c0f96ac5852adb88d678fd16d650a34d88d5a633366e0c69287c5c22deef5d17&=&format=webp&quality=lossless&width=932&height=524)</br></br>

The `Profiles` tab is completely up to you.</br>
`Overlay` I have set to `Full`, with the `Time` parameter set to `Off`.</br>
I have set up custom hotkeys which I find intuitive, so here is a few screens of my `Hotkeys` tab:
![image](https://media.discordapp.net/attachments/1069768559699431525/1264002390655504454/image.png?ex=669c4975&is=669af7f5&hm=b4c9d61c580443713683cbb63426cc1a3a46742a735c245dbcecd1cdb7af3ecc&=&format=webp&quality=lossless&width=932&height=524)</br>
![image](https://media.discordapp.net/attachments/1069768559699431525/1264002481629823086/image.png?ex=669c498b&is=669af80b&hm=9d9914c3083c88d8ca1bcfbea5409b8c02e817d5753eb86461fce406795f0fca&=&format=webp&quality=lossless&width=932&height=524)</br>
![image](https://media.discordapp.net/attachments/1069768559699431525/1264002582217490522/image.png?ex=669c49a3&is=669af823&hm=e96e75d3a501d2ffee3e329c2993294dddc07e9fdfc04caed49f2b9662747672&=&format=webp&quality=lossless&width=932&height=524)</br>
![image](https://media.discordapp.net/attachments/1069768559699431525/1264002734869319710/image.png?ex=669c49c8&is=669af848&hm=c6db1a680323d6e6673899ae1150c6cb8608395d5d27aee750d6f6bbf8c1465e&=&format=webp&quality=lossless&width=932&height=524)</br></br>

In `Settings` at the bottom, be sure to switch `On` the `Auto-start application`, `Open application in background` and `Close minimizes`.  Scroll to the bottom of the `Settings` page and switch `Off` the `RivaTuner Statistics Server` toggle.</br></br>

Handheld Companion is now configured!  It can be safely minimized (if you set up custom hotkeys as shown, use the `L1 + R1 + R3` combo!)</br></br>

### Winaero Tweaker

Winaero Tweaker is a UI for Windows settings and registry tweaks which will improve performance and declutter the UI.  Customize your Windows install with an easily-reversible check box.</br>
Install the application and reboot.  Once you are back, launch Winaero Tweaker as Admin and start customizing.</br>
My custom settings file is pasted here in plaintext.  Read it to see what is being changed.  I have disabled Windows Update for maximum stability.  If you would like the same on your system, copy and paste it into your favorite text editor and Save As a .ini file.  Within the Winaero app, select `File -> Import/Export` and select your .ini file.  Once you complete the wizard and reboot, Cortana/Copilot will be disabled, as well as background tasks and Windows Update.</br>
```
[Format]
ProductName=Winaero Tweaker
ProductVersion=1.63.0.0
FormatVersion=1.1
[User]
pageWin11ClassicContextMenus=1
pageDisableCopilot=1
pageAdsUnwantedApps=1
pageDisableLookInStore=1
pageDisableSmartScreen=1
pageOneDriveDisableUserFolderBackup=1
pageTaskbarClockShowSeconds=1
pageDisableWebSearch=1
pageChrEdgeDisableDesktopShortcut=1
pageChrEdgeDisableUpdates=1
pageDefenderTrayIcon=1
pageDisableCortana=1
pageDisableWindowsInk=1
pageDisableTelemetry=1
pageDisableSpotlightDesktopIcon=1
pageContextMenuSafeMode=1
pagePowerThrottling=1
pageDefender=1
pageDisableOnlineVideoTips=1
pageHideInsiderPage=1
pageRestorePointFrequency=1
pageErrorReporting=1
pageDisableMRT=1
pageDisableSafeZoneInformation=1
pageDisableAutomaticMaintenance=1
pageBackgroundApps=1
pageDisableDriverUpdates10=1
pageWindowsUpdate=1
[pageDisableCopilot]
IsCopilotButtonDisabled=1
IsCopilotDisabled=1
[pageAdsUnwantedApps]
UnwantedAppsDisabled=1
FileExplorerAdsDisabled=1
LockScreenAdsDisabled=1
StartSuggestionsDisabled=1
TipsAboutWindowsDisabled=1
WelcomePageDisabled=1
SettingsAdsDisabled=1
TimelineSuggestionsDisabled=1
[pageDisableSmartScreen]
DisableSmartScreen=1
DisableSmartScreenInEdge=1
DisableSmartScreenInStore=1
[pageDefenderTrayIcon]
DefenderTrayIconEnabled=0
```
</br>

This is all that is needed for Winaero Tweaker to function.  Remember to reboot! 

### Bonus Registry Tweaks & Uninstalling Windows Apps

These are some custom registry tweaks which I have enabled to allow faster internet speeds. This is system/setup dependent, however my Steam download speed went from 10Mbps to 80Mbps.</br></br>

First, I added a value for IRPStackSize.  This can lower ping and increase overall throughput.
Open the Registry Editor with `Win + R` and typing `regedit`.  Navigate to this registry entry `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters`.  Right click on the folder `Parameters` and create a new DWORD (32-bit) by selecting `New -> DWORD (32-bit) Value`.  Enter the `Value name:` as `IRPStackSize` and set the value as `32 (decimal)`.  Click `OK` to apply the value.</br></br>

Next, I changed the default TTL to 64.  This combines with the other registry edit to increase speeds.
Within Registry Editor navigate to the entry `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters`.  Right click on the folder `Parameters` and select `New -> DWORD (32-bit) Value`.  Name it `DefaultTTL` and value it `64 (decimal)`.</br></br>
 
Close Registry Editor and reboot your PC.  Now you should have increased internet speeds!

For Windows apps, I use [Revo Uninstaller](https://download.revouninstaller.com/download/RevoUninstaller_Portable.zip), it has batch select and automatic registry backups.  I like this software and use it often, I got a pro key even though the free version is feature complete imo.  

### Conlcusion

That covers all the tweaks and settings which I have configured on my Win4!</br></br>
Contact me on Discord in the [GPD Devices server](https://discord.com/invite/gpd-devices-243411108940087297).
I have [CashApp](https://cash.app/$twerkules) if you like this and want more Win4 content and guides.</br>
