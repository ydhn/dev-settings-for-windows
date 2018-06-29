# dev-settings-for-windows

## Hyper
- hyper.js https://hyper.is/
- hyperstart.bat https://gist.github.com/legowerewolf/a3e0eb7830752488fec329c7bdcb2d2a
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

## Git
- Use git on wsl as default https://github.com/andy-5/wslgit
