# Audio CD ripping on Linux

We only want native apps with AccurateRip support: [whipper](https://github.com/whipper-team/whipper), [rubyripper](https://github.com/bleskodev/rubyripper), [fre:ac](https://github.com/enzo1982/freac)

## whipper

* Requirements: [Inital config](https://github.com/whipper-team/whipper#getting-started)

```bash
whipper cd rip
```

# Downloading audio of a yt video as mp3

* Requirements:
```
$ sudo apt install python3-pip
$ pip3 install --user yt-dlp
```

This will convert yts native format (m4a / ogg) no matter what to mp3 using ffmpeg / avconv / ffprobe / avprobe (depending on your distribution).

## Single vidoes

`yt-dlp -f bestaudio --extract-audio --audio-format mp3 --audio-quality 0 <Video-URL>`

## Playlists

`yt-dlp --ignore-errors --format bestaudio --extract-audio --audio-format mp3 --audio-quality 0 --output "%(title)s.%(ext)s" --yes-playlist <playlist-url>`
