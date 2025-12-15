# ATTENTION

I forked this project because it wouldn't compile for MacOS 15.2 (24C101)
I made some fixes to make it possible.

A command-line tool to manage default applications for file types on macOS. It provides an interactive interface to set default applications for individual file extensions or groups of related file types (like video, audio, images, etc.).

&copy; 2025, [Vitalii Tereshchuk][home] 

## How to Install and Use

Download the file `dutis-macos.tar.gz` from the `Releases` section and unzip it.
Inside the archive there is a file `dutis` which you should copy to `/usr/local/sbin` or `/usr/local/bin`

I prefer to use `~/.local/bin`
So you need to run the command:

```
chmod +x ./dutis
sudo xattr -rd com.apple.quarantine ./dutis
cp ./dutils ~/.local/bin
```

## Build  from source

Another way is a local build.

```
git clone https://github.com/xvoland/dutis.git
cd dutis
cargo build --release
```

If the build was successful, you can find the compiled file in

```
cd target/release
chmod +x ./dutis
cp ./dutis ~/.local/bin
```




# ⚠️ Donation

No matter if I get the money or not, I'm gonna keep making the app better 'cause I love seeing folks use it and reach their goals.<br />
And you know what? Every $1 really makes a difference for folks like me.<br />
It helps cover stuff like domain hosting and the hours I put into coding, which would be super awesome and free up some more family time. Thanks a bunch!

### Crypto

**BTC (ERC20):** 0x17496b75d241d377334717f8cbc16cc1a5b80396<br />
**USDT (TRC20):** TAAsGXjNoQRJ7ewxSBL2W3DUCoG7h8LCT6


### Other

[Donate here for my projects][paypal]

<a href='https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=9D4YBRWH8QURU'><img alt='Click here to lend your support to my projects and make a donation!' src='https://www.paypalobjects.com/en_US/GB/i/btn/btn_donateCC_LG.gif' border='0' /></a>

<br />
<br />


# ☎️ Connect with me:

### Social
[<img align="left" alt="xVoLAnD" width="50px" src="https://raw.githubusercontent.com/xvoland/xvoland/main/images/logo-dotoca.svg" />][home]
[<img align="left" alt="xvoland | Instagram" width="50px" src="https://raw.githubusercontent.com/xvoland/xvoland/main/images/instagram.svg" />][instagram]
[<img align="left" alt="Vitalii Tereshchuk | YouTube" width="50px" src="https://raw.githubusercontent.com/xvoland/xvoland/main/images/youtube.svg" />][youtube]

<br />
<br />

<hr />

# Dutis

[![CI](https://github.com/tsonglew/dutis/actions/workflows/ci.yml/badge.svg)](https://github.com/tsonglew/dutis/actions/workflows/ci.yml)
[![License](https://img.shields.io/github/license/tsonglew/dutis)](https://github.com/tsonglew/dutis/blob/master/LICENSE)
[![Crates.io](https://img.shields.io/crates/v/dutis)](https://crates.io/crates/dutis)
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/tsonglew/dutis)](https://github.com/tsonglew/dutis/releases)

A command-line tool to manage default applications for file types on macOS. It provides an interactive interface to set default applications for individual file extensions or groups of related file types (like video, audio, images, etc.).

> ⚠️ **Note**: This tool is designed specifically for macOS and will not work on other operating systems.

> ⚠️ **Warning**: This tool relies on deprecated macOS CoreServices APIs (deprecated since macOS 10.4–12.0). While it currently works, it may become unstable or stop working in future macOS versions. Apple has not provided direct replacements for these APIs, making this the only available approach for programmatically managing file type associations.

## Features

- 🎯 Set default applications for individual file extensions
- 👥 Batch set default applications for groups of file types (video, audio, image, etc.)
- 🔍 Interactive selection of applications
- 🎨 Color-coded output for better visibility
- ⚡ Fast and efficient Rust implementation
- 🔄 Supports common file type groups out of the box

## Installation

### Using Homebrew (recommended)

```shell
brew tap tsonglew/dutis
brew install dutis
```

### Using Cargo

```shell
cargo install dutis
```

### Building from Source

```shell
git clone https://github.com/tsonglew/dutis.git
cd dutis
cargo build --release
```

## Usage

### Basic Usage

```shell
# Set default application for a single file extension
sudo dutis <file-extension>

# Example: Set default application for .mp4 files
sudo dutis mp4
```

### Group Mode

```shell
# Set default application for a group of file types
sudo dutis --group <group-name>

# Example: Set default application for all video files
sudo dutis --group video
```

> ⚠️ **Note**: `sudo` is required because changing default applications requires system-level permissions.

### Available Groups

The following file type groups are supported:

- `video`: Common video formats (mp4, avi, mkv, etc.)
- `audio`: Audio formats (mp3, wav, aac, etc.)
- `image`: Image formats (jpg, png, gif, etc.)
- `code`: Programming and markup files (py, js, rs, etc.)
- `archive`: Archive formats (zip, tar, gz, etc.)

You can view the full list of supported extensions in the `config/groups.yaml` file.

## Configuration

Dutis uses a YAML configuration file to define file type groups. The default configuration is located at `config/groups.yaml`. You can modify this file to add or remove file extensions from groups.

Example group configuration:

```yaml
groups:
  video:
    - mp4
    - avi
    - mkv
    # ...
  audio:
    - mp3
    - wav
    - aac
    # ...
```

## Requirements

- macOS operating system
- Rust 1.56 or later (for building from source)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


## 📺 You can also watch my Latest YouTube Videos:

<!-- YOUTUBE:START -->
- [🎄 Cozy Christmas Fireplace 24/7 | Relaxing Christmas Music &amp; Crackling Fire 🔥](https://www.youtube.com/watch?v=Y_YAzZJsNys)
- [Create 3D Dioramas in Nano Banana Pro Photoshop AI  #gemini3pro #photoshop #tutorial #design](https://www.youtube.com/shorts/PapDyWzcobQ)
- [Create Hyper-Realistic 3D Dioramas in Photoshop with Nano Banana Pro &lpar;Step-by-Step Tutorial&rpar;](https://www.youtube.com/watch?v=CA9uAnR46vM)
- [Typography &lpar;Mosaic&rpar; Portrait with Nano Banana &lpar;Gemini 3&rpar; in Adobe Photoshop  #photoshop #tutorial](https://www.youtube.com/shorts/et2bmRH5UPY)
- [🍌  How to Create Typography &lpar;Mosaic&rpar; Portrait with Nano Banana &lpar;Gemini 3&rpar; in Adobe Photoshop](https://www.youtube.com/watch?v=3jNAjMiQw3A)
<!-- YOUTUBE:END -->

[home]: http://dotoca.net
[homepage]: https://dotoca.net/shuffle-files
[githubreleases]: https://github.com/xvoland/shuffle-files/releases
[paypal]: https://paypal.me/xvoland
[youtube]: https://youtube.com/xvoland
[instagram]: https://www.instagram.com/xvoland/
