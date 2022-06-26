# public-notes

- Browser URL or filepath string: Ctrl+L
- VScode zoom: Ctrl++ and Ctrl+-
- To disable vim in vscode: F1 or Ctrl + Shift + P, Toggle vim mode
- Move window: Win key + Arrow key

- To search a file name in cmd

```
dir/s *filename*
```

- To search string in all files, filename, dir name

```bash
findstr /I /S stringtosearchhere * > outputfiletostoreresult.txt
Get-ChildItem -Recurse | Select-String -Pattern stringtosearchhere
```

- To get playlist names in youtube

```
Not working:
 youtube-dl -o '%(playlist_index)s - %(title)s.%(ext)s' <url or id here> --get-filename

Working:
Only to get file name:
 youtube-dl -o "%(playlist_index)s-%(title)s.%(ext)s" PL6n9fhu94yhUbctIoxoVTrklN3LMwTCmd --get-filename
To download videos with number prefixed:
 youtube-dl -o "%(playlist_index)s-%(title)s.%(ext)s" PL6n9fhu94yhUbctIoxoVTrklN3LMwTCmd

```

- Retrieve plugin log
  https://xxxxx.api.crm.dynamics.com/api/data/v9.1/plugintracelogs?$top=1&$orderby=createdon%20desc

- vsdiff compare

```
"C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\Common7\IDE\CommonExtensions\Microsoft\TeamFoundation\Team Explorer\vsDiffMerge.exe" "C:\Users\<user-name>\Desktop\Left.txt" "C:\Users\<user-name>\Desktop\Right.txt" \t
```

- vscode settings.json Preferences

```javascript
{
    "window.zoomLevel": 1,
    "editor.formatOnSave": true,
    // Command Prompt
    // "terminal.integrated.shell.windows": "C:\\Windows\\System32\\cmd.exe"
    // Git Bash
    "terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",
    "[json]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "vim.insertModeKeyBindings": [
        {
            "before": [
                "k",
                "j"
            ],
            "after": [
                "<Esc>"
            ]
        }
    ],
    "vim.useSystemClipboard": true
}
```

- Vim .vimrc setting

```
inoremap kj <Esc>
set number
colo torte
syntax on
set clipboard=unnamed
```

- Toggle maximized panel: Ctrl + Alt + T
- Toggle terminal: Ctrl + `

- Windows shutdown for linux
```
shutdown /s /t 0
```

- VS Code shortcuts
`Ctrl+Shift+L` - Select all occurrences and edit

> List of helpful shortcuts for faster coding

If you have any other helpful shortcuts, feel free to add in the comments of this gist :)

## Official List of all commands

* [Windows](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)
* [Mac](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)

## Open/View

Open Command Pallete

```bash
Shift+Cmd+P
Shift+Ctrl+P
```

Access Settings

```bash
Cmd+,
Ctrl+,
```

Toggle Terminal

```bash
Ctrl+`
Ctrl+`
```

Create New Terminal
```
Shift+Ctrl+`
Shift+Ctrl+`
```

Toggle Sidebar

```bash
Cmd+B 
Ctrl+B
```

Open New Window/Instance

```bash
Shift+Cmd+N 
Shift+Ctrl+N
```

Close Window

```bash
Cmd+W 
Ctrl+W
```

## Working With Files

Sidebar Focus

```bash
Shift+Cmd+E
Shift+Ctrl+E
```

Open File/Folder From Sidebar
```
Cmd+Down
Ctrl+Down
```

Change File Tabs

```bash
Ctrl+Tab 
Ctrl+PageUP
```

Quick File Open

```bash
Cmd+P
Ctrl+P
```

Open File From Explorer

```bash
Cmd+O
Ctrl+O
```

New File

```bash
Cmd+N
Ctrl+N
```

Save

```bash
Cmd+S
Ctrl+S
```

Save As

```bash
Shift+Cmd+S
Shift+Ctrl+S
```

Close File

```bash
Cmd+W
Ctrl+W
```

Delete File
```
Cmd+Delete
Ctrl+Delete
```

Reopen Files
```
Shift+Cmd+T
Shift+Ctrl+T
```

Zoom

```bash
Cmd++ # Zoom in
Cmd+- # Zoom out

Ctrl++ # Zoom in
Ctrl+- # Zoom out
```

Spilt Editor

```bash
Cmd+\
Ctrl+\
```

## Code Editing

Go To Start & End Of Line

```bash
Cmd+Right
Cmd+Left

Ctrl+Right
Ctrl+Left

home
end
```

Move By Word

```bash
Option+Right
Option+Left

Alt+Right
Alt+Left
```

Go To Start & End Of File

```bash
Cmd+Up
Cmd+Down

Ctrl+Home
Ctrl+End
```

Cut, Copy & Past Line

```bash
Cmd+X #Cut
Cmd+C #Copy
Cmd+V #Paste

Ctrl+X # Cut
Ctrl+C # Copy
Ctrl+V # Paste
```

Move Line Up & Down

```bash
Option+Up
Option+Down

Alt+Up
Alt+Down
```

Copy Line Up & Down

```bash
Shift+Option+Up
Shift+Option+Down

Shift+Alt+Up
Shift+Alt+Down
```

Remove Line

```bash
ShiftCmd+K
Shift+Ctrl+K
```

Insert Line

```bash
Cmd+Enter # Insert below
Shift+Cmd+Enter # Insert above

Ctrl+Enter # Insert below
Shift+Ctrl+Enter # Insert above
```

Jump To Matching Bracket

```bash
Shift+Cmd+\
Shift+Ctrl+\
```

Add Line Comment

```bash
Cmd+/
Ctrl+/
```

Add Block Comment

```bash
Shift+Option+A
Shift+Alt+A
```

Highlight Code

```bash
Shift+Any Direction
```

Select Next Match

```bash
Cmd+D
Ctrl+D
```

De-select Match

```bash
Cmd+U
Ctrl+U
```

Add Cursor

```bash
Option+Click
Alt+Click
```

Go to Entity (Functions, vars, etc)

```bash
Cmd+Shift+O
Ctrl+Shift+O
```

