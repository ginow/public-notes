# public-notes
- PDF compress command
  ```bash
  gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 \
   -dPDFSETTINGS=/screen \
   -dDownsampleColorImages=true \
   -dColorImageDownsampleType=/Bicubic \
   -dColorImageResolution=130 \
   -dDownsampleGrayImages=true \
   -dGrayImageDownsampleType=/Bicubic \
   -dGrayImageResolution=130 \
   -dDownsampleMonoImages=true \
   -dMonoImageDownsampleType=/Subsample \
   -dMonoImageResolution=130 \
   -dNOPAUSE -dBATCH -dQUIET \
   -sOutputFile=output.pdf input.pdf
  ```
  
- To search a file name in cmd

```
dir/s *filename*
```

- To search string in all files, filename, dir name

```bash
findstr /I /S stringtosearchhere * > outputfiletostoreresult.txt
```
```powershell
Get-ChildItem -Recurse | Select-String -Pattern stringtosearchhere
```
```javascript
// Get all <a> elements within the playlist
var playlistItems = document.querySelectorAll('#items a');

// Array to store URLs
var urls = [];

// Iterate over each <a> element
playlistItems.forEach(function(item) {
    // Check if the href attribute exists and starts with "/watch"
    var href = item.getAttribute('href');
    if (href && href.startsWith && href.startsWith('/watch')) {
        // Add the URL to the array
        href=`python C:\Users\user\youtube-dl -x --audio-format mp3 --ignore-errors "https://www.youtube.com${href}"`;
        urls.push(href);
    }
});

// Convert the array of URLs to a string
var urlsText = urls.join('\n');

// Create a Blob containing the URLs
var blob = new Blob([urlsText], { type: 'text/plain' });

// Create a temporary URL to download the Blob
var url = URL.createObjectURL(blob);

// Create a link element to trigger the download
var link = document.createElement('a');
link.href = url;
link.download = 'playlist_urls.txt';

// Append the link to the document body and trigger the download
document.body.appendChild(link);
link.click();

// Cleanup: remove the link and revoke the Blob URL
document.body.removeChild(link);
URL.revokeObjectURL(url);
```
- Retrieve plugin log
  https://xxxxx.api.crm.dynamics.com/api/data/v9.1/plugintracelogs?$top=1&$orderby=createdon%20desc

## vscode settings.json Preferences

- Cursor blinking `phase`
- Editor: Cursor Smooth Caret Animation `on`
- Editor › Sticky Scroll: Enabled

```json
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
    "vim.useSystemClipboard": true,
    // Paste image directly into markdown:
     "markdown.copyFiles.destination": {
        "**/*": "${documentWorkspaceFolder}/assets/"
    }
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


### VS Code vim shortcuts
`gd` go to definition
`Ctrl+O` go back to previous view 

### VS Code shortcuts

Toggle Sidebar

```bash
Ctrl+B
```

Sidebar Focus

```bash
Shift+Ctrl+E
```

Fold unfold

```bash
Ctrl+Shift+[
```

`Ctrl+Shift+L` - Select all occurrences and edit

## Official List of all commands

* [Windows](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)

## Open/View

Open Command Pallete

```bash
Shift+Ctrl+P
```

Access Settings

```bash
Ctrl+,
```

Toggle Terminal

```bash
Ctrl+`
```

Create New Terminal
```
Shift+Ctrl+`
```


Open New Window/Instance

```bash
Shift+Ctrl+N
```

Close Window

```bash
Ctrl+W
```

## Working With Files


Open File/Folder From Sidebar
```
Ctrl+Down
```

Change File Tabs

```bash
Ctrl+PageUP
```

Quick File Open

```bash
Ctrl+P
```

Open File From Explorer

```bash
Ctrl+O
```

Save As

```bash
Shift+Ctrl+S
```

Close File

```bash
Ctrl+W
```

Delete File
```
Ctrl+Delete
```

Reopen Files
```
Shift+Ctrl+T
```

Spilt Editor

```bash
Ctrl+\
```

## Code Editing

Go To Start & End Of Line

```bash
Ctrl+Right
Ctrl+Left
```

Move By Word

```bash
Alt+Right
Alt+Left
```

Go To Start & End Of File

```bash
Ctrl+Home
Ctrl+End
```

Cut, Copy & Past Line

```bash
Ctrl+X # Cut
Ctrl+C # Copy
Ctrl+V # Paste
```

Move Line Up & Down

```bash
Alt+Up
Alt+Down
```

Copy Line Up & Down

```bash
Shift+Alt+Up
Shift+Alt+Down
```

Remove Line

```bash
Shift+Ctrl+K
```

Insert Line

```bash
Ctrl+Enter # Insert below
Shift+Ctrl+Enter # Insert above
```

Jump To Matching Bracket

```bash
Shift+Ctrl+\
```

Add Line Comment

```bash
Ctrl+/
```

Add Block Comment

```bash
Shift+Alt+A
```

Select Next Match

```bash
Ctrl+D
```

De-select Match

```bash
Ctrl+U
```

Add Cursor

```bash
Alt+Click
```

Go to Entity (Functions, vars, etc)

```bash
Ctrl+Shift+O
```

- Browser URL or filepath string: Ctrl+L
- VScode zoom: Ctrl++ and Ctrl+-
- To disable vim in vscode: F1 or Ctrl + Shift + P, Toggle vim mode
- Move window: Win key + Arrow key

- Windows shutdown for linux
```
shutdown /s /t 0
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
