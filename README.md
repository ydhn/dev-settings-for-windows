# dev-settings-for-windows

## Hyper
- hyper.js https://hyper.is/
- hyperstart.bat https://gist.github.com/legowerewolf/a3e0eb7830752488fec329c7bdcb2d2a
```bat
@ECHO off
:top
CLS
ECHO Choose a shell:
ECHO [1] Windows Subsystem for Linux (Ubuntu 18.04)
ECHO [2] Git bash
ECHO [3] PowerShell
ECHO [4] cmd
ECHO.
ECHO [5] restart elevated
ECHO [6] exit
ECHO.

CHOICE /N /C:123456 /M "> "
CLS
IF ERRORLEVEL ==6 GOTO end
IF ERRORLEVEL ==5 powershell -Command "Start-Process hyper -Verb RunAs"
IF ERRORLEVEL ==4 cmd
IF ERRORLEVEL ==3 powershell
IF ERRORLEVEL ==2 "C:\Program Files\Git\git-cmd.exe" --command=usr/bin/bash.exe -l -i
IF ERRORLEVEL ==1 bash --login -c zsh

CLS
ECHO Switch or exit?
ECHO [1] Switch
ECHO [2] Exit

CHOICE /N /C:12 /D 2 /T 5 /M "> "
IF ERRORLEVEL ==2 GOTO end
IF ERRORLEVEL ==1 GOTO top

:end
```
- .hyper.js
```js
colors: {
    black: '#000000',
    red: '#C51E14',
    green: '#1D6621',
    yellow: '#C7C329',
    blue: '#0ABBFF',
    magenta: '#C839C5',
    cyan: '#20C5C6',
    white: '#C7C7C7',
    lightBlack: '#686868',
    lightRed: '#FD6F6B',
    lightGreen: '#67F86F',
    lightYellow: '#FFFA72',
    lightBlue: '#6A76FB',
    lightMagenta: '#FD7CFC',
    lightCyan: '#68FDFE',
    lightWhite: '#FFFFFF',
},
//shell: 'C:\\Windows\\System32\\bash.exe',      // WSL as default
//shellArgs: ['--login', '-c', 'zsh', '-i', '-l'], // WSL as default
shell: '', // CMD
shellArgs: ['/C', 'C:\\Users\\yundo\\hyperstart.bat'],
```

## Git with Visual Studio Code
- Use git on wsl as default https://github.com/andy-5/wslgit

## Docker
https://nickjanetakis.com/blog/setting-up-docker-for-windows-and-wsl-to-work-flawlessly
