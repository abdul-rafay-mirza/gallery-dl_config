# My Personal gallery-dl Configuration

This repository contains my personal [gallery-dl](https://github.com/mikf/gallery-dl) configuration.

## Features

- Saves downloaded files in the current directory.
- Custom filenames for:
  - Twitter/X downloads:
    ```
    twitter_<author>_(@<username>)_<tweet_id>.<extension>
    ```
  - Pixiv downloads:
    ```
    pixiv_<illustration_id>_p<page>.<extension>
    ```
- Runs `figlet "done!"` after each completed download.
- Automatically writes the source URL into downloaded files using `exiftool`:
  - `Artist`
  - `XPAuthor`
  - `XMP:Creator`
  - It stores the source URL of the image in the "Authors" section of the metadata (at least that's what Windows calls it). Works reliably for both JPEG's and PNG's
    
  ![Screenshot of the Details Section in Properties showing the Authours field being filled up](https://media.discordapp.net/attachments/1080819163905392702/1524443344053338132/image.png?ex=6a506cc0&is=6a4f1b40&hm=9f30393abe7864af26a56b038844a5aade699cbcf864163a03f0fb8a1c0882e3&=&format=webp&quality=lossless&width=639&height=92)

## Requirements

- `gallery-dl`
- `exiftool`
- `figlet`

Make sure both `exiftool` and `figlet` are available in your system's `PATH`.

## Installation

Clone this repository or copy the configuration into the following path for your Operating System:


## Installation

Copy the configuration file to one of the following locations.

### Windows

`gallery-dl` checks these locations (in order):

```text
%APPDATA%\gallery-dl\config.json
%USERPROFILE%\gallery-dl\config.json
%USERPROFILE%\gallery-dl.conf
```

> **Note:** `%USERPROFILE%` is your home directory (for example, `C:\Users\<username>`).

### Linux / macOS

```text
/etc/gallery-dl.conf
${XDG_CONFIG_HOME}/gallery-dl/config.json
${HOME}/.config/gallery-dl/config.json
${HOME}/.gallery-dl.conf
```

You can also clone this repository and copy the configuration to whichever location `gallery-dl` uses on your system.

## Notes

This configuration is intended for my own workflow. It is intentionally minimal.
Feel free to use it as a starting point and customize it to your own needs.
