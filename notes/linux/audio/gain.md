# Set gain audio files under Linux
Add audio gain tags for different audio formats under linux.

## r128gain

Currently (r128gain)[https://github.com/desbma/r128gain] is my favourite because it's hit&run.

### Install

```bash
pip3 install --user r128gain
source ~/.profile
```

### Usage

```
r128gain -r . # add track gain for all files in folder
r128gain -r -a . # add track and album gain for all files in folder

```
