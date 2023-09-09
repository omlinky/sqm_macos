# Gui for sqlmap
# SQLmap Command Builder for macOS

[![Python 3.x](https://img.shields.io/badge/python-3.x-yellow.svg)](https://www.python.org/) [![License](https://img.shields.io/badge/license-GPLv2-red.svg)](https://github.com/omlinky/sqm_macos/blob/main/LICENSE)

This is simple GUI for sqlmap based on old Chinese version of SQLmap Command Builder.

## Supported OS:

- macOS only

## Requirements:

- Python 3

## How to prepeare the file:

Attention! It's a little bit tricky to run SQLmap Command Builder on macOS but it's possible

- Check your python3 version
```sh
python3 --version
```

- Install appscript
```sh
sudo pip3 install appscript
```

- You can put files of SQLmap Command Builder in sqlmap folder or manually change sqlmap intallation folder:
- Open sqm.pyw in any text file editor, for example: SublimeText, Coda2, BBEdit, or any other, even in standart macOS text editor
- go to line 20
```python
sqlmap_path = "./"
```
- you have to change instllation path "./" to your sqlmap installation path. Example: My installation directory of sqlmap
- be awared that the /omlinky/ is my username, you will have yours
```python
sqlmap_path = "/Users/omlinky/Desktop/sqlmap-dev"
```
- or you can uncomment next line that contains homebrew installation path of sqlmap
```python
#sqlmap_path = "./"
sqlmap_path = "/opt/homebrew/opt/sqlmap/libexec/"
```

## How to run
- Download sqlmap. Here /Users/omlinky/Desktop/sqlmap-dev change omlinky to your username macOS
```sh
git clone --depth 1 https://github.com/sqlmapproject/sqlmap.git /Users/omlinky/Desktop/sqlmap-dev
```
- Give necessary permissions if nedeed
```sh
chmod u+x /Users/omlinky/Desktop/sqlmap-dev
```
- Put all files of SQLmap Command Builder in sqlmap folder
- Go to sqlmap installation folder
```sh
cd /Users/omlinky/Desktop/sqlmap-dev
python3 sqm.pyw
```

## How to run with Homebrew
- Git this repo to your mac
```sh
git clone --depth 1 https://github.com/omlinky/sqm_macos /Users/omlinky/Desktop/sqm_macos
```
- Install sqlmap with Homebrew
```sh
brew install sqlmap
```
- Run script with python
```sh
cd /Users/omlinky/Desktop/sqm_macos
python3 sqm.pyw
```

## Troubleshoot
- If you use pyenv, use [this manual](https://stackoverflow.com/a/61879759) to install tkinter properly.

All video instructions and updates announces you can find on my twitter 
```sh
@omlinky
```
