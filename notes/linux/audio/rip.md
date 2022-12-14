# Audio CD ripping on Linux

We only want native apps with AccurateRip support: [whipper](https://github.com/whipper-team/whipper), [rubyripper](https://github.com/bleskodev/rubyripper), [fre:ac](https://github.com/enzo1982/freac)

## whipper

* Requirements: [Inital config](https://github.com/whipper-team/whipper#getting-started)

```bash
whipper cd rip
```

# Downloading audio of a yt video as mp3

* Requirements: `sudo pacman -S youtube-dl`

This will convert yts native format (m4a / ogg) no matter what to mp3 using ffmpeg / avconv / ffprobe / avprobe (depending on your distribution).

`youtube-dl -f bestaudio --extract-audio --audio-format mp3 --audio-quality 0 <Video-URL>`
