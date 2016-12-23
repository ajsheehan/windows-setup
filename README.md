# Applications
First install Chocolatey
## Chocolatey
	$ set-ExecutionPolicy RemoteSigned
	$ iwr https://chocolatey.org/install.ps1 -UseBasicParsing | iex
	$ choco feature enable -n=allowGlobalConfirmation

## Chrome
	$ choco install googlechrome

## Git
	$ choco install git

## GitKraken
    $ choco install gitkraken

## Node.js
    $ choco install nodejs

## Notepad++
    $ choco install notepadplusplus

## Postman
	$ choco install postman

## Slack
	$ choco install slack

## Spotify
    $ choco instasll spotify

## SQL Server Management Studio
	$ choco install sql-server-management-studio

## Visual Studio Code
	$ choco install visualstudiocode
### Plugins
Launch VS Code Quick Open ```ctrl + p``` then enter the following

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