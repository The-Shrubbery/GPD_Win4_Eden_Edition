# GPD Win4 - Eden Edition
Improve FPS, temps, and battery life on your GPD Win4!

## Setup Guide for GPD Win4, updated in July 2024

![image](https://www.gizmochina.com/wp-content/uploads/2022/09/GPD-Win-4-White-Silver-1.png)

<!-- GETTING STARTED -->
## Getting Started

If performance on your Win4 is not as expected, this guide will hopefully help resolve your issues and provide some useful tips on using the powerful softwares available for our amazing handheld.</br>
</br>
The softwares referenced in this guide are:</br>
[**AMD Adrenaline**](https://www.amd.com/en/support/download/drivers.html)</br>
[**Rivatuner Statistics Server**](https://www.guru3d.com/download/rtss-rivatuner-statistics-server-download/)</br>
[**Motion Assistant**](https://drive.google.com/file/d/1X4CrqWz2VKiyHlwPI32oQrqUarWi6jTG/view?usp=sharing)</br>
[**Auto TDP**](https://cdn.discordapp.com/attachments/993089115245514783/1239066546022776922/TDP-399.zip?ex=669be0e5&is=669a8f65&hm=dfbf1538e1a3291df0ee27ebdb37882fa490999289205710b03746774b262182&)</br>
[**Handheld Companion** ](https://github.com/Valkirie/HandheldCompanion/releases)</br>
Optional:</br>
[**Winaero Tweaker**](https://winaero.com/downloads/winaerotweaker.zip)</br>
[**Revo Uninstaller**](https://download.revouninstaller.com/download/RevoUninstaller_Portable.zip)</br></br>


As we proceed through the guide we will be installing and configuring each of these softwares in order.</br>
If any of these are already installed on your system, please make sure they are all up to date!</br></br>

![image](https://github.com/user-attachments/assets/a6634248-e00a-48f6-a94c-54880ab28578)


### AMD Adrenaline

Adrenaline is the official AMD driver controller and configuration software.  It comes installed by default with driver updates and offers automatic configuration of your settings, performance monitoring, and AMD exclusive feature access (also available with AutoTDP, though my testing showed better stability and consistency with Adrenaline installed).</br>

The UI is quite large in this app, so it requires a few more screens.</br>
![image](https://github.com/user-attachments/assets/8cec05d7-9a8b-4c10-8b15-1d50f267d6e4)</br>
![image](https://github.com/user-attachments/assets/e5e43902-d00a-4924-8a86-b82ef7861b4d)</br>
![image](https://github.com/user-attachments/assets/72d53de7-4cf8-4518-9eba-7ccfa2a7dc2c)</br></br>

I keep most of the AMD features `Off` for lower overhead.  Super Resolution, however, is a must.  Excellent upscaling, and the Win4 will run almost anything at 720p so I consider this option requisite.  Anti-Lag I have enabled as well, it prioritizes 3D applications in the Windows input queue and can provide lower input delay.</br>
- `Vsync on` is a good idea, enabling it here works well with Anti-Lag.</br>
- `Anti-Aliasing` set to `Enhance` with `Morphological - Enabled` provides huge visual benefit to FXAA/Low settings with very low overhead.  Its basically Super Resolution for AA!</br>
- Since the Win devices have so much VRAM for a portalble, we can set `Anastropic Filtering` to `Enabled, x16` without any performance difference and max visual quality.  `Texture Filtering Quality` can be maxed out as well thanks to this VRAM!</br>
- `Tessellation Mode` relies on VRAM as well and thus can be set to max.  This controls how well 3D models and textures are blended together/overlayed, it makes a huge difference in overall detail with very little impact to performance.</br>
- In Adrenaline, under `Settings -> Display`, disable everything except `GPU Scaling` and set the `Scaling Mode` to `Preserve aspect ratio`, this gives best performance and compatability.</br>
![image](https://github.com/user-attachments/assets/281db04e-1839-4295-8090-7eccee4ee562)</br></br>

- In `Settings -> Preferences`, set your options as shown in this screenshot.  Avoid annoying pop ups!</br>
![image](https://github.com/user-attachments/assets/ff17475f-15e7-410e-ab10-7874fa028d5c)</br></br>

Adrenaline is now configured to be as unobtrusive as possible and can be used to do driver updates.  Some apps benefit from Fluid Motion Frames, though my setup here provides similar FPS without the input lag or compatability woes of AMFM.</br></br>


### Rivatuner Statistics Server

Rivatuner, or RTSS, is a commonly used frametiming software.  It basically does the same thing as Vsync, but is effective across the whole system.  Other applications in this guide require the software for full functionality, and it requires minimal setup!</br></br>

Simply [download](https://www.guru3d.com/download/rtss-rivatuner-statistics-server-download/) and install the software, reboot once it has finished installing.</br>
- Once you are back online, open RTSS and in the main window select `Start with Windows` to switch it `ON`.  In the `Framerate Limit` box, click and type `60`, then hit `Enter`.</br></br>
![image](https://github.com/user-attachments/assets/dc89a190-c1c9-4620-ad2b-9f0675f6f066)</br></br>
Your RTSS should be set up and can be safely **minimized** to the background.


### Motion Assistant

Motion Assistant is the official GPD software, it has firmware control over some of the functions on your Win system, and ideally is installed **but not running in the background!** </br>  
In fact, Motion Assistant should not be running at all in order to get best performance.  This is a "set-and-forget" configuration! </br>

Firstly we must install / update the software from [the GPD Google Drive](https://drive.google.com/file/d/1X4CrqWz2VKiyHlwPI32oQrqUarWi6jTG/view?usp=sharing).</br>
- Once the software is installed, open it and navigate to the TDP tab.  This is where we will do most of our work, configuring emulated controllers and hotkeys will be covered later in the guide using a different software.</br>
- Set your software to the settings shown here:</br>
![image](https://github.com/user-attachments/assets/0e43e8cd-3dcd-4b53-86bc-2811d887112d)</br></br>

- Check and uncheck the `Auto Lock GPU`, `Optimize GPU`, and `Custom Float GPU` to be sure the options are set according to the screenshot.  Fill out empty fields or input the value again and hit `Enter` to ensure everything is set like the screenshot.</br>
- Next, click the `Unlock GPU` button and press `OK` on the dialogue box to hibernate your system.  Wait for it to turn off, then bring it back from hibernate.  This allows the other softwares to control the GPU!</br>
- Ensure `Start with windows` is **UN-checked** to prevent Motion Assistant from interfering with the rest of this setup.</br>
Your Motion Assistant should be set up!  Close Motion Assistant and make sure it is not minimized or running in your Task Tray.</br></br>

Note:</br>
If your `FPS Limit` text is greyed out, install [**RTSS**](https://www.guru3d.com/download/rtss-rivatuner-statistics-server-download/) as mentioned previously.  Be sure you have **rebooted** after the installation for RTSS to talk with Motion Assistant.

### AutoTDP

Ciphray's AutoTDP.bat file is a custom made utility that does some obscure magic which makes Windows perform much much better!  Cannot thank you enough, Ciphray.</br>
Installing is extremely easy: simply extract the .zip file to a folder of your choice (I have a folder in My Documents called "TDP"), then run `TDP_UV_MENU_FAST.bat` to bring up the main menu.</br>
![image](https://github.com/user-attachments/assets/83ff9d2d-85d5-43e1-b230-7bb37d23f4a9)</br>
If your settings look different than the screenshot, do not mind it at all.  In the next section we will configure all that.  Check back after finishing the guide and see your changes reflected in the TDP Menu!</br></br>

From the TDP Menu do the following key combinations on your Win4: </br>
- `R -> 0` to enable `Core Performance Boost`.  This will allow your system its max power output based on demand.  Make sure the option is `Enabled`.</br>
- Next, press `M -> 1` to open advanced Windows settings and disable Superfetch.  This indexes your entire SSD and tries to dynamically cache frequently used files and apps so your computer "responds faster".  Much better to disable on a gaming device.</br>
- Once that operation completes and the screen refreshes, press `2` and wait for refresh.  This brings back the full right-click context menu.  Better usability imo.</br>
- After that has refreshed the screen, press `3` and `4` to prevent Windows from showing a pop up every time you switch between mouse and controller mode, and prevents the controller from navigating the Windows UI.  We have a keyboard and mouse nub!  Wait for the menu to refresh between presses and once these are complete, press `Q` twice to get back to the main menu.</br>
- From the main menu, input on the keyboard `S -> I -> E` and wait a few moments.  This change adds Ciphray's custom power profiles to Windows.  These prevent Windows from changing the `EPP` value, which controls the power balance between CPU and GPU on a 0-100% scale where 0% is all CPU and 100% is all GPU.  We will do fine control of this value with Handheld Companion, this step just forces Windows out of the way.  Make sure the `Cycle Power Scheme Currently` value is set to `Power Saver-EPP` by pressing the `F` key as needed.  Press `Q` to return to the main menu.</br>
- Next, press `Y -> 7` to open the AC/DC power mode menu.  Press `1`, `2`, and `3` as needed so each value is set to `Max Performance`, then press `A` to save settings. 
 If you return to this menu it **will not** reflect your custom settings, even though they are applied!  I had to ask Ciphray about this lol.</br></br>

Once you are back to the main menu, press `Q` to exit without selecting a TDP.  All settings will persist through reboots and are effective even if AutoTDP.bat is not running.  Reboot to ensure your settings are applied.  AutoTDP is now configured on your Win4!

### Handheld Companion

Handheld Companion controls system performance, emulated controllers, and performance overlay.  This app is where you do all TDP and fan curve customization, and supports per-applicaiton profiles.</br>
- Firstly after installing the software and rebooting, open Handheld Companion and make sure your emulated controller is behaving correctly and not showing multiple inputs.</br>
- Next, go in to the `Device` tab and enable the `Controllable power (cTDP) override`.  Set the values to `5` for min and `35` for max.</br>
- The `Performance` tab has all the action.  Here are a pair of screenshots of the performance tab, configure your system to follow these settings:
![image](https://github.com/user-attachments/assets/4cd5551f-29fc-47ff-95c6-bf564448abcb)</br>
![image](https://github.com/user-attachments/assets/facfe607-7a79-4b30-82c7-a8469617cbb4)</br>
- Your TDP should adjust by itself thanks to AutoTDP, however if you are getting low CPU/GPU usage try to toggle the `Automatic TDP` setting to `60fps`.</br>
![image](https://github.com/user-attachments/assets/20e2183c-912d-415c-9b73-5c3942b66d14)</br>
- This fan curve works well for me at minimizing noise while keeping temps low-ish.  Never gone above 90C with this config, though the average is a much cooler 80C. 
 I do use [these grips](https://www.shapeways.com/product/WJ632EHE7/gpd-win-4-grips) which mitigate heat quite a lot, so adjust these curves to your comfort.</br></br>

The `Profiles` tab is completely up to you.</br>
- `Overlay` I have set to `Full`, with the `Time` parameter set to `Off`.</br>
- I have set up custom hotkeys which I find intuitive, so here is a few screens of my `Hotkeys` tab:
![image](https://github.com/user-attachments/assets/2a0e274e-18a1-4e66-ba86-770aeee267e2)</br>
![image](https://github.com/user-attachments/assets/46044c08-b05d-45a6-a730-51ec2908f853)</br>
![image](https://github.com/user-attachments/assets/19cd6ba5-9112-4521-90d1-de9e826da797)</br>
![image](https://github.com/user-attachments/assets/cad490d4-18fd-4017-bd30-a3a567afae59)</br></br>

- With this setup, pressing the shoulder buttons allows access to all system shortcuts.  I also set my back keys to Fullscreen and Task View using WinControl and entering thes key combo set in Handheld Companion.  Set your WinControl like this for maximum convenience:</br>
![image](https://github.com/user-attachments/assets/04d7184b-40a5-43d0-af7f-c9c5e224cb1c)</br></br>

- Back in Handheld Companion, select `Settings` at the bottom.  Switch `On` the `Auto-start application`, `Open application in background` and `Close minimizes` options, then scroll to the bottom of the page and switch `Off` the `RivaTuner Statistics Server` toggle.</br></br>

Handheld Companion is now configured!  It can be safely minimized (if you set up custom hotkeys as shown, use the `L1 + R1 + R3` combo!)

### Winaero Tweaker

Winaero Tweaker is a UI for Windows settings and registry tweaks which will improve performance and declutter the UI.  Customize your Windows install with an easily-reversible check box.</br>
Install the application and reboot.  Once you are back, launch Winaero Tweaker as Admin and start customizing.</br>
My custom settings file is pasted here in plaintext.  Read it to see what is being changed, they are pretty self explanitory, and more detail can be found in the Winaero app.  The settings file here disables background tasks, internet searching in the start menu, OneDrive user folder uploads, and Cortana/Copilot to name a few.</br>
Overall I aim to disable all the background apps and invasive telemetry Windows 11 likes to send.  This also greatly lowers the overhead of Windows OS.</br>
Most importantly, my settings disable Windows Update.  This provides maximum stability and prevents random updates from interrupting your game and breaking your install.</br>
- If you would like the same on your system, copy and paste the below block into your favorite text editor and Save As an .ini file.  Within the Winaero app, select `File -> Import/Export` and select your .ini file.  Once you complete the wizard and reboot, Cortana/Copilot will be disabled, as well as background tasks and Windows Update.</br>
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

These are some custom registry tweaks which I have enabled to allow faster internet speeds. This is system/setup dependent, however my Steam download speed went from 10Mbps to 80Mbps on both my Win4 systems and laptops, works on my mobile tether as well.</br></br>

First, I added a registry value for IRPStackSize.  This can lower ping and increase overall throughput by decreasing the size of individual data packets then processing them at a faster rate.</br>
- Open the Registry Editor with `Win + R` and typing `regedit`.  Navigate to this registry entry `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters`.  Right click on the folder `Parameters` and create a new DWORD (32-bit) by selecting `New -> DWORD (32-bit) Value`.  Enter the `Value name:` as `IRPStackSize` and set the value as `32 (decimal)`.  Click `OK` to apply the value.</br></br>

Next, I changed the default TTL to 64.  TTL, or Time To Live, indicates to the internet what kind of device the packet originated from, and controls the queue priority for each packet across the entire internet.  This combines with the other registry edit to increase speeds by signaling your device as an Android mobile and thus higher queue priority.</br>
- Within Registry Editor navigate to the entry `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters`.  Right click on the folder `Parameters` and select `New -> DWORD (32-bit) Value`.  Name it `DefaultTTL` and value it `64 (decimal)`.</br></br>
 
- Close Registry Editor and reboot your PC.  Now you should have increased internet speeds!</br></br>

For Windows apps, I use [Revo Uninstaller](https://download.revouninstaller.com/download/RevoUninstaller_Portable.zip), it has batch select and automatic registry backups.  I like this software and use it often, I got a pro key even though the free version is feature complete imo.</br>
- Once the app is installed, open Revo and select `Windows apps` from the bottom left corner.  Check the box next to each app you would like to remove and click `Uninstall`.  Follow the wizard, unchecking `Create restore point` and checking `Create full registry backup` and `Automatically delete all found leftovers`.  Click `Ok` to remove the app, then click `Scan` to check for leftover files.  You may have the option to select `Scan all accounts for leftovers` in the bottom right corner, make sure the box is checked for maximum uninstalling.  Reboot and your system will be free of annoying useless software!</br><br>


### Conlcusion

That covers all the tweaks and settings which I have configured on my Win4!</br></br>
- Contact me on Discord in the [GPD Devices server](https://discord.com/invite/gpd-devices-243411108940087297) @`The Shrubbery`. </br>
- I have [CashApp](https://cash.app/$twerkules) if you like this and want more Win4 content and guides.</br>
