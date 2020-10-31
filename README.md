# public-notes
* Browser URL or filepath string: Ctrl+L
* VScode zoom: Ctrl++ and Ctrl+-
* To disable vim in vscode: F1 or Ctrl + Shift + P, Toggle vim mode
* Move window: Win key + Arrow key

* To search a file name in cmd
```
dir/s *filename*
```
* To search string in all files, filename, dir name
```bash
findstr /I /S stringtosearchhere * > outputfiletostoreresult.txt
Get-ChildItem -Recurse | Select-String -Pattern stringtosearchhere 
```
* To  get playlist names in youtube
```
 youtube-dl -o '%(playlist_index)s - %(title)s.%(ext)s' <url or id here> --get-filename
```
* Retrieve plugin log
https://xxxxx.api.crm.dynamics.com/api/data/v9.1/plugintracelogs?$top=1&$orderby=createdon%20desc

* vsdiff compare
```
"C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\Common7\IDE\CommonExtensions\Microsoft\TeamFoundation\Team Explorer\vsDiffMerge.exe" "C:\Users\<user-name>\Desktop\Left.txt" "C:\Users\<user-name>\Desktop\Right.txt" \t
```
* vscode settings.json Preferences
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
* Toggle maximized panel: Ctrl + Alt + T
* Toggle terminal: Ctrl + `