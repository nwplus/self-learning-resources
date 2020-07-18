# 💻 What is the command line/terminal/shell?

Most modern computer operating systems such as Windows and OS X provide a graphical user interface that enables us to open and view files, play music, and browse the web all through simple movements and clicks of the mouse.

However, there's a much lesser known way of navigating those same things: the command line interface or the CLI. 

The command line is the stereotypical 'hackerman' terminal that you see in all those movies. It's a way to interface with your computer through text.

<p align="center">
  <img src="https://media0.giphy.com/media/26gssNZ4EF6c8Simk/giphy.gif" alt="cmd challenge"/>
</p>

In fact, you can do most — if not everything — through a command line that you can do through a pointing and clicking and using windows. Using the command line has a lot of its own benefits too. some things like installing things are as easy as a few keystrokes whereas you would normally have to go through navigating to a website, downloading an installer, and following all the steps.

# 🤔 How do I use it?

## Mac and Linux
### Getting Started

Mac → You can boot up a new command line by searching up 'Terminal' in Launchpad

Linux → You can press ```CTRL+ALT+T``` to open a new Terminal

### Basic commands
- Navigating folders

  ```cd``` → is short for 'change directory'. If you were to compare it back to the graphical interface, its much like navigating and clicking through folders through your file explorer.
  
  When specifying a directory to change to, you can use either absolute or relative path names. The absolute or full path starts from the system root ```/```, and relative path starts from your current directory.
  
  Usually when you start a new Terminal, you are in the ```home``` directory, commonly denoted as ```~```
  
  You can navigate into folders by doing ```cd name-of-folder```, and even nested folders by doing ```cd name-of-folder/nested-folder```
  
  You can go back one level of folders by doing ```cd ..``` and multiple levels by doing ```cd ../..```
  
  Still confused? No worries! There are lots of resources that give you lots of information about ```cd```. Here are a few:
  - [https://linuxize.com/post/linux-cd-command/](https://linuxize.com/post/linux-cd-command/)
  
  ```ls``` → is short for 'list'. This command tells you what files are in your current working directory. If you are in the home directory, the output will look something like this:
  
  ```bash
  → ls
  Applications
  Desktop
  Downloads
  Library
  Music
  Files
  Documents
  Movies
  Pictures
  ```

- Copying, moving, and deleting files and folders

  ```cp``` → is short for 'copy'. This command lets you copy files and folders from one location to another. You can copy single files from A to B by doing ```cp A B```. For example, if you want to copy a file from your Downloads into your home folder, it would look something like

  ```bash
  # copy a file from Downloads into the Home directory
  cp ~/Downloads/example.txt ~
  ```
  
  If you need to copy an entire folder,  you can add the ```-r``` flag.
  
  ```bash
  # copy a folder inside Downloads to the current folder
  # you can reference current location using `.`
  cp -r ~/Downloads/example_folder .
  ```
  
  ```mv``` → is short for 'move'. The commands follow the same format as ```cp```
  
  ```rm``` → is short for 'remove'. The commands follow the same format as ```mv``` and ```cp```
  
- Creating files and folders
  ```touch``` → creates new, empty files. For example, ```touch example.txt``` will create a new empty file with the name ```example.txt``` in the current directory.
  ```mkdir``` → is short for 'make directory' and makes a new folder. For example, ```mkdir folder-name``` will create an empty folder with the name ```folder-name``` in the current directory.
  
- Viewing file contents
  ```cat``` → is short for 'concatenate' but really we just use it to print out file contents. Say you had a file called ```README.md``` and you wanted to quickly view what the contents of it were, you could do ```cat README.md``` and it would print out its contents into the terminal. If it's too long, you can do ```cat README.md | less``` so that it scrolls.
  
- Editing file contents
  ```nano``` → a simple text editor in the terminal. If you want to quickly edit the contents of a README, a Python script, or anything really, you can do ```nano file-name``` to edit it. When you're finished, press ```CTRL+X``` and save if you'd like.

### Package Managers
Hate downloading installers? Wish you could just download and install stuff just from your command line? Package managers may be for you!
- ```apt``` (Linux)
  ```apt``` is a package manager that comes pre-installed with Linux. It makes it super easy to install packages and other stuff. You can install a new package by doing ```sudo apt install <package_name>```. For example, if you wanted to install ```pip```, a Python package manager for Python 3, you can just do ```sudo apt install python3-pip```. To uninstall, you can just do ```sudo apt purge python3-pip```.
  
  You can find more info here: [https://itsfoss.com/apt-command-guide/](https://itsfoss.com/apt-command-guide/)
  
 - ```brew``` (Mac)
  Homebrew is the "missing package manager for macOS". Basically, it lets you manage, install, and remove software super easily through the command line. To install it, paste this into your terminal
  ```bash
  # install homebrew
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
  ```
  Then, installing packages is as easy as ```brew install python```. To uninstall, it's as easy as ```brew uninstall python```.
  
  You can read more here: [https://brew.sh/](https://brew.sh/)
 
## Windows
### Basic commands
Recommended to get Windows Terminal → linux-like terminal on your windows machine! [This](https://www.microsoft.com/en-ca/p/windows-terminal/9n0dx20hk701) will let you follow the more detailed instructions in the Mac and Linux toggle above.

If you want to just stick with the regular Windows terminal, you can find some guides on what it can do by searching for "MS DOS commands".

[https://www.c3scripts.com/tutorials/msdos/commands.html](https://www.c3scripts.com/tutorials/msdos/commands.html)

## More resources
If you're still curious and want to learn more about the fancy command line, here are a list of great resources to help you dive deeper.
- [https://missing.csail.mit.edu/2020/command-line/](https://missing.csail.mit.edu/2020/command-line/)
