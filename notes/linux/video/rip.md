# Backup your yt video / playlist

* Requirements: `sudo pacman -S youtube-dl`

This backups your yt video as mp4 file with m4a audio. This compatible with most modern media players like TVs.

`youtube-dl -f 'bestvideo[ext=mp4]+bestaudio[ext=m4a]/best[ext=mp4]/best' -o '%(title)s.%(ext)s' <video/playlist link>`
