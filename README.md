# public-notes
- Check NVIDIA GPU Utilisation in Debian
  ```bash
  nvidia-smi
  ```
- Run any app using NVIDIA
  ```bash
  prime-run blender
  ```
- If unable to do `git clone` on mounted drives then do:
  ```bash
  sudo umount /mnt/new_volume
  lsblk
  sudo mount -o rw,uid=1000,gid=1000,dmask=0022,fmask=0133 /dev/sdb1 /mnt/new_volume
  ```
  Note that lsblk is to find out the name "sdb1"
- Push git changes to remote: First check if SSH is setup in GitHub for your user
  ```bash
  ssh -T git@github.com #Hi ginow! You've successfully authenticated, but GitHub does not provide shell access.
  git remote add <anyname> git@github.com:ginow/<repo-name>.git
  ```
- PDF compress command, using ghostscript command
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
- If C# VS Code extensions not working properly then add below in `settings.json`
  ```
   "dotnetAcquisitionExtension.existingDotnetPath": [
        
        {
            "extensionId": "ms-dotnettools.csharp",
            "path": "/home/predator/.dotnet/dotnet"
        }
    ]
  ```
- Retrieve plugin log
  https://xxxxx.api.crm.dynamics.com/api/data/v9.1/plugintracelogs?$top=1&$orderby=createdon%20desc

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
