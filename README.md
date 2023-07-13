## Description

If you new formatted your computer on Windows 10 Pro, Windows 11, you can run this script.

This script does exactly the following; (Some are optional(y/n))

<details><summary>Windows Updates</summary>&nbsp;

- It asks if you want to make windows updates.

  </details>

<details><summary>System Settings</summary>&nbsp;

- It asks if you want Region change to Turkey.  
- It asks if you want change your hostname.
- It asks if you want disable Windows Defender.
- Date format is set to turkey
- Getting the Old Classic Right-Click Context Menu (For Windows 11)
- Disabling News and Interes on Taskbar
- Default Old Photo Viewer
- Setting Dark Mode for Applications
- Setting Dark Mode for System
- Setting Control Panel View to Large Icons
- Enabling NumLock After Startup
- Disabling Windows Beep Sound
- Disabling IPv6 stack
- Disabling Startup Apps
- Setting Cloud Flare DNS
- Hiding People Icon from Taskbar
- Hiding Taskview Icon from Taskbar
- Hiding MultiTaskview Icon from Taskbar
- Showing Small Icons in Taskbar
- Hiding Taskbar Search
- Removing Chat from Taskbar
- Removing Widgets from Taskbar
- Taskbar Aligns Left (For Windows 11)
- Hiding Recycle Bin Shortcut from Desktop
- Disabling hiberfil.sys
- Disabling Display and Sleep Mode Timeouts
- Disabling Windows Defender
- Disabling Updates for Other Microsoft Products
- Disabling Cortana
- Disabling Bing Search in Start Menu
- Disabling SmartScreen Filter
- Disabling Sensors
- Disabling Tailored Experiences
- Disabling Xbox Gamebar
- Disabling Xbox Features
- Disabling Blocking of Downloaded Files
- Setting 'This PC' for File Explorer
- Expanding for File Explorer
- Disabling Nightly Wake-up for Automatic Maintenance
- Disabling Storage Sense
- Unpinning all Start Menu tiles
- Disabling Built-in Adobe Flash in IE and Edge
- Disabling Edge Preload
- Disabling Internet Explorer First Run Wizard
- Disabling Windows Media Player Online Access
- Showing Known File Extensions
- Disabling Action Center (Notification Center)
- Disabling System Restore for System Drive
- Setting Low UAC Level
- Removing Unnecessary Tasks
- Enabling Clearing of Recent Files on Exit
- Disabling Recent Files Lists
- Disabling Search for App in Store for Unknown Extensions
- Hiding 'Recently added' List from the Start Menu
- Stopping and Disabling Unnecessary Services
- Setting Desktop Wallpaper
- Show All Icons on Taskbar
- Copy Files to Documents
- Importing Startup task in Task Scheduler

</details>

<details><summary>Privacy Settings</summary>&nbsp;
  
- Disabling Telemetry
- Blocking Telemetry in Host File
- Disabling Feedback
- Disabling Activity History
- Disabling Website Access to Language List
- Stopping and Disabling Connected User Experiences and Telemetry Service
- Disabling Advertising ID
- Disabling Wi-Fi Sense
- Disabling Application Suggestions
- Disabling UWP Apps Background Access
- Disabling Access to Voice Activation from UWP Apps
- Disabling Access to Notifications from UWP Apps
- Disabling Access to account Info from UWP Apps
- Disabling Access to Contacts from UWP Apps
- Disabling Access to Calendar from UWP Apps
- Disabling Access to Phone Calls from UWP Apps
- Disabling Access to Call History from UWP Apps
- Disabling Access to Email from UWP Apps
- Disabling Access to Tasks from UWP Apps
- Disabling Access to Messaging from UWP Apps
- Disabling Access to Radios from UWP Apps
- Disabling Access to Other Devices from UWP Apps
- Disabling Access to Diagnostic Information from UWP Apps
- Disabling Access to Libraries and File System from UWP Apps
- Disabling UWP Apps Swap File
- Disabling Automatic Maps Updates
- Disabling Windows Update Automatic Restart
- Disabling Windows Update Automatic Downloads

</details>
<details><summary>Install Softwares</summary>&nbsp;
  
It asks if you want to install the following softwares or not.

- Winget for Windows 10
- Mozilla Firefox
- Opera
- Google Chrome
- Libre Wolf
- Brave Browser
- Steam
- Epic Games
- HWMonitor
- Crystal Disk Info
- VMWare Workstation Pro
- VirtualBox
- Signal Desktop
- Softwares for developers(MSVS Community, MSVS Buildtools, WindowsSDK, NodeJS, Python and Git)
- Microsoft Visual Studio Code (with extensions)
- AnyDesk
- Windows Terminal
- Speedtest
- Sublime Text 4
- Github Desktop
- VLC Media Player
- TreeSize Free
- Total Commander
- Rufus
- Wireshark
- PuTTY
- Deluge
- DBeaver
- Cryptomator
- Microsoft Teams
- Powertoys
- DupeGuru
- WinFsp for Cryptomator
- 7-Zip
- Lightshot
- Twinkle-Tray
- K-Lite Codec Pack Mega
- Nvidia GeForce Experience
- Malwarebytes
- Internet Download Manager
- CloudFlare WARP
- Valorant

</details>

<details><summary>Remove Unused Apps/Softwares</summary>&nbsp;
  
- Uninstalling Default Third Party Applications
- Uninstalling Windows Media Player
- Uninstalling Work Folders Client
- Uninstalling Microsoft XPS Document Writer
- Removing Default Fax Printer
- Uninstalling OneDrive
- Removing Microsoft Edge
- Uninstalling Windows Fax and Scan Services
- It asks if you want uninstall Windows OneDrive.
- It asks if you want uninstall Windows Edge.

</details>

<details><summary>Startup Script</summary>&nbsp;
  
This script adds a task named 'startup' to the task scheduler. This task does exactly the following;

- Remove En-US Keyboard
- Adding Turkey Keyboard
- Importing Previously Set Task to Task Scheduler
- Removing Stick Keys
- Removing Toggle Keys
- Remove Unnecessary Tasks(update and such) in Task Scheduler.(It also adds task to delete Unnecessary Tasks on every boot)
- Sync Windows Localtime
- Update apps (browsers, apps, softwares and such..) with WinGet&nbsp;
  
```vbs
Set WshShell = CreateObject("WScript.Shell") 
WshShell.Run chr(34) & "C:\startup\Run.cmd" & Chr(34), 0
Set WshShell = Nothing
```

</details>

<details><summary>My Custom Drivers</summary>&nbsp;

```diff
🟠 When this question is asked, you must answer by saying 'n'. Because the settings here 
are my specific settings.
```

&nbsp;
&nbsp;
</details>

```json
NOTE:
! Before running the script, you need to turn off Windows defender's real-time protection setting once.
```

![alt text](https://github.com/caglaryalcin/caglaryalcin/blob/main/win-def.jpg)

```diff
! This script takes about 35 minutes with 100mbps internet.
```

## Start the script

####

If IE is never started after the PC is formatted, the script will not run because the config files are not created. To ignore it, this command must be executed first.

```
Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Internet Explorer\Main" -Name "DisableFirstRunCustomize"
```

#### Defines the link of the script as a variable

```
$ScriptFromGitHub = Invoke-WebRequest https://raw.githubusercontent.com/caglaryalcin/after-format/main/Shells.psm1
```

#### Starts the script

```
Invoke-Expression $($ScriptFromGitHub.Content)
```
