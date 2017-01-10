# Settings
## Show File Extensions
Using PowerShell
```powershell
$key = 'HKCU:\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced'
Set-ItemProperty $key Hidden 1
Set-ItemProperty $key HideFileExt 0
Set-ItemProperty $key ShowSuperHidden 1
Stop-Process -processname explorer
```

# Applications
First install Chocolatey
## Chocolatey
	$ set-ExecutionPolicy RemoteSigned
	$ iwr https://chocolatey.org/install.ps1 -UseBasicParsing | iex
	$ choco feature enable -n=allowGlobalConfirmation

## Chrome
	$ choco install googlechrome

## Firefox
    $ choco install firefox

## Git
	$ choco install git

## GitKraken
    $ choco install gitkraken

## ngrok
1. Install ngrok

        $ choco install ngrok.portable

2. Restart PowerShell and authenticate

        $ ngrok authtoken {{authtoken}}

3. Update the ngrok config with desired tunnels

        $ code $HOME/.ngrok2/ngrok.yml

```
tunnels:
  {{tunnelname}}:
    proto: http
    addr: {{port}}
    host_header: localhost
```

## Node.js
    $ choco install nodejs

## NuGet CLI
    $ choco install nuget.commandline

## Postman
	$ choco install postman

## Slack
	$ choco install slack

## Spotify
    $ choco instasll spotify

## SQL Server Management Studio
	$ choco install sql-server-management-studio

## Visual Studio
    $ choco install visualstudio2015enterprise
Function to open solution from PowerShell

1. Open PowerShell profile in VS Code

        $ code $profile

2. Add the following function and save

```powershell
function vs($path = '.')
{
    Write-Host $path;
    $s = ls $path *.sln -Rec | select -First 1;
    if($s)
    {
        start $s.FullName
    }
}
```

## Visual Studio Code
	$ choco install visualstudiocode
### Plugins
Launch VS Code Quick Open ```ctrl + p``` then enter the following

    $ ext install c#
    $ ext install theme-cobalt2

### settings.json
```javascript
// Place your settings in this file to overwrite the default settings
{

// Editor

    // Zoom the font of the editor when using mouse wheel and holding Ctrl
    "editor.mouseWheelZoom": true,

// Window

    // Controls how folders are being reopened after a restart. Select 'none' to never reopen a folder, 'one' to reopen the last folder you worked on or 'all' to reopen all folders of your last session.
    "window.reopenFolders": "none",

// Files

    // Configure glob patterns of file paths to exclude from file watching. Changing this setting requires a restart. When you experience Code consuming lots of cpu time on startup, you can exclude large folders to reduce the initial load.
    "files.watcherExclude": {
        "**/.git/objects/**": true,
        "**/node_modules/**": true
    },

// Search

    // Configure glob patterns for excluding files and folders in searches. Inherits all glob patterns from the files.exclude setting.
    "search.exclude": {
        "**/node_modules": true,
        "**/bower_components": true
    },

// Integrated Terminal

    // Controls the font family of the terminal, this defaults to editor.fontFamily's value.
    "terminal.integrated.fontFamily": "Inconsolata for Powerline"
}
```

# Bloatware
Uninstall Windows 10's built-in apps
## 3D Builder
    $ Get-AppxPackage *3dbuilder* | Remove-AppxPackage

## Alarms and Clock
    $ Get-AppxPackage *windowsalarms* | Remove-AppxPackage

## Calculator
    $ Get-AppxPackage *windowscalculator* | Remove-AppxPackage

## Calendar and Mail
    $ Get-AppxPackage *windowscommunicationsapps* | Remove-AppxPackage

## Camera
    $ Get-AppxPackage *windowscamera* | Remove-AppxPackage

## Get Office
    $ Get-AppxPackage *officehub* | Remove-AppxPackage

## Get Skype
    $ Get-AppxPackage *skypeapp* | Remove-AppxPackage

## Get Started
    $ Get-AppxPackage *getstarted* | Remove-AppxPackage

## Groove Music
    $ Get-AppxPackage *zunemusic* | Remove-AppxPackage

## Maps
    $ Get-AppxPackage *windowsmaps* | Remove-AppxPackage

## Microsoft Solitaire Collection
    $ Get-AppxPackage *solitairecollection* | Remove-AppxPackage

## Money
    $ Get-AppxPackage *bingfinance* | Remove-AppxPackage

## Movies & TV
    $ Get-AppxPackage *zunevideo* | Remove-AppxPackage

## News
    $ Get-AppxPackage *bingnews* | Remove-AppxPackage

## OneNote
    $ Get-AppxPackage *onenote* | Remove-AppxPackage

## People
    $ Get-AppxPackage *people* | Remove-AppxPackage

## Phone Companion
    $ Get-AppxPackage *windowsphone* | Remove-AppxPackage

## Photos
    $ Get-AppxPackage *photos* | Remove-AppxPackage

## Store
    $ Get-AppxPackage *windowsstore* | Remove-AppxPackage

## Sports
    $ Get-AppxPackage *bingsports* | Remove-AppxPackage

## Voice Recorder
    $ Get-AppxPackage *soundrecorder* | Remove-AppxPackage

## Weather
    $ Get-AppxPackage *bingweather* | Remove-AppxPackage

## Xbox
    $ Get-AppxPackage *xboxapp* | Remove-AppxPackage