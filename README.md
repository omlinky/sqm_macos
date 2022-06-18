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

- Open sqm.pyw in any text file editor, for example: SublimeText, Coda2, BBEdit, or any other, even in standart macOS text editor
- go to line 22
```sh
appscript.app('Terminal').do_script('python3 /Users/your_folder_to_sqlmap/sqlmap.py --update')
```
- you have to change your_folder_to_sqlmap to your sqlmap installation folder. Example: My installation directory of sqlmap 
```sh
/Users/omlinky/Desktop/sqlmap-dev
```
- Be awared that the /omlinky/ is my username, you will have yours
- Than you have to change the code line like this
```sh
appscript.app('Terminal').do_script('python3 Users/omlinky/Desktop/sqlmap-dev/sqlmap.py --update')
```
- Do the same with line 5150
```sh
appscript.app('Terminal').do_script('python3 /Users/your_folder_to_sqlmap/sqlmap.py %s' % (self.sqlEdit.get()))
```
- Where your_folder_to_sqlmap is exact way to your sqlmap installation directory
```sh
appscript.app('Terminal').do_script('python3 Users/omlinky/Desktop/sqlmap-dev/sqlmap.py' % (self.sqlEdit.get()))
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
- Put  all files of SQLmap Command Builder in sqlmap folder
- Go to sqlmap installation folder
```sh
cd /Users/omlinky/Desktop/sqlmap-dev
python3 sqm.pyw
```

All video instructions and updates announces you can find on my twitter 
```sh
@omlinky
```
