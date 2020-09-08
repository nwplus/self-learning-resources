# 🟦 Windows

There's a bit more context we need to know to get started with the command line on a Windows machine, but a PC is still great for software development. While on a Mac or Linux we have access to a kind of shell called "bash" from the get go, on Windows we instead have the Command Prompt (CMD) and PowerShell. While you can install a version of bash on your machine, here I'll assume you do not have access to bash. If you do, you're welcome to follow the steps from the section on Mac/Linux setup.

## Getting started

For just about everything, you'll want to use PowerShell. It's a bit more advanced than CMD, works really well for the tasks most common for a developer, and is a bit fancier under the hood, allowing you to pass "richer" information between commands.

To open PowerShell, simply head to the Windows search bar and type in PowerShell. You can also use it as an integrated terminal within your favorite IDE, such as VS Code.

## Basic commands

- Navigating folders
  - `cd` → See the [Mac/Linux description](/2-beginner/command-line-mac-linux.md) for more info.
  - `ls` → See the [Mac/Linux description](/2-beginner/command-line-mac-linux.md) description for more info.
- Copying, moving, and deleting files and folders
  - `cp` → See the [Mac/Linux description](/2-beginner/command-line-mac-linux.md) description for more info.
  - `mv` → See the [Mac/Linux description](/2-beginner/command-line-mac-linux.md) description for more info.
  - `rm` → See the [Mac/Linux description](/2-beginner/command-line-mac-linux.md) description for more info.
- Creating files and folders
  - `ni` → To create a new file, run `ni <file>`, such as, `ni example.txt`. 
  - `md` → To create a new directory, run `md <directory>`, such as, `md example`. 
- Viewing file contents
  - `cat` → See the [Mac/Linux description](/2-beginner/command-line-mac-linux.md) description for more info.
- Editing file contents
  - `notepad` → To edit a text file or see some content in plaintext, run `notepad <file>`, such as `notepad example.txt`.

Note that for a lot of these commands, even though they look the same as their Mac/Linux equivalent, they're actually just aliases for other PowerShell commands. For example, `rm` in PowerShell actually runs `Remove-Item`. You can see this for yourself by typing `Get-Alias rm` into PowerShell.

What does this mean for you? Well, sometimes, if you copy and paste a `rm ...` from the internet, it might not work, since `Remove-Item` behaves a little differently than bash `rm`. However, there is a way to use bash directly on a Windows computer to avoid this headache. More on that at the end of the "Package Managers" section!

### An aside

Want to look like a real hacker on Windows?

1. Open Windows search and type in "run", and open Run, or alternatively, hit Windows + R.
2. Type "cmd" into run and hit enter.
3. Run `color a`.
4. Run `tree`.
5. (Hit CTRL + C to stop the tree.)

If this doesn't impress your non-techie friends, what will!

## Package Managers

As is mentioned in the Mac and Linux section, package managers are great for being able to manage all of the software you need as a developer: editors, tools, applications, and more. Microsoft is [actively developing](https://github.com/microsoft/winget-cli) a package manager available in the Microsoft Store called "[winget](https://www.microsoft.com/en-us/p/app-installer/9nblggh4nns1?activetab=pivot:overviewtab)", but for now, the most commonly used package manager is chocolatey.

Chocolatey makes installing new software as easy as `choco install <package>`. Setting up chocolatey is a bit involved. Instructions are available [on their website](https://chocolatey.org/install), and I'll tried to provide some added context here.

1. Head to the Windows search bar and type in PowerShell; in the right-hand menu, click run as administrator.
2. To paste into PowerShell, with something already copied to your clipboard (highlight, CTRL+C) you simply right-click in the shell. Copy and paste the following command into PowerShell: 
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))`
```
3. Wait for the command to complete.
<img style="display: block; margin: 0 auto;" src="https://i.ytimg.com/vi/U7CZcd-UYmU/mqdefault.jpg" alt="One eternity later..." />
4. And you're finished!

From here, we can install some really helpful tools that we can use in the command line.

| Software | Command | Why use it? |
|---|---|---|
| [git](https://chocolatey.org/packages/git) | `choco install git` | The world's most popular version control software. |
| [Windows Terminal](https://chocolatey.org/packages/microsoft-windows-terminal/1.1.2233.0) | `choco install microsoft-windows-terminal` | A (new) terminal for Windows to allow you to interact with multiple shells, organize tabs, and more, in a friendly way. | 
| [cURL](https://chocolatey.org/packages/curl) | `choco install curl` | A command line interface for interacting with APIs. More on this in the intermediate section! | 
| [GNU make](https://chocolatey.org/packages/make) | `choco install make` | A replacement for Linux's [make](https://opensource.com/article/18/8/what-how-makefile), allowing you to use a given makefile. |

<h3>A <span style="text-decoration: line-through;">birthday</span> bash</h3>

Once you've installed Git on a Windows device, you also get access to git bash. There are other "bashes" (for example, through [Cygwin](https://cygwin.com/index.html) or through [WSL](https://docs.microsoft.com/en-us/windows/wsl/about), which aren't covered here), but since we already know so much about PowerShell, git bash is more than sufficient. 

Open git bash by searching "bash" in the Windows search bar and hitting enter.

## The path

After a while of using the command line, you'll start to notice we can almost "add" commands to it by installing certain applications. For example, if you install Python, a popular programming language, on your computer, you'll then be able to type `python` into your terminal, and your terminal won't throw an error. What gives?

On Windows, this is managed through a special variable called your PATH. It specifies a set of paths (such as C:\Program Files\Python) where executable programs can be found, such as `python.exe`. It effect, it gives you shortcuts to executable files than you can then access from your command line by just typing in their name. So, instead of typing out `C:\Program Files\Python` every time you'd like to run a Python program, you can simply just type `python`.

This is especially important because one of the most common errors you'll encounter in PowerShell is the following:

<p style="color: red;">"The term '...' is not recognized as the name of a cmdlet, function, script file, or operable program. Check the spelling of the name, or if a path was included, verify that the path is correct and try again."</p>

If this happens, don't panic! Google is your friend here. Try searching "add ... to PATH" (replace "..." with the name of what you're trying to execute) and follow what comes up. Typically, `choco` will automatically add things to your path, so you won't have to worry about this. If you're sure you've already added it to your path and your still not working, you can refresh PowerShell by typing `refreshenv`.

## Next steps for Windows

Want to go further with your Windows configuration? Check out these resources to learn how to install the Windows Subsystem for Linux, to run Linux right on your Windows machine, customize your terminal with fonts and pretty colors, create terminal aliases to save some key strokes, and more, with these resources:

### Better terminal emulators [(link)](https://docs.microsoft.com/en-us/windows/terminal/)

"Terminal emulator" is a common way of referring to programs that act as terminals, but are a bit fancier than a "standard" terminal. One common one has already been mentioned a few times: Windows Terminal. It's available for download from the Microsoft Store, and is a fantastic option. After it is installed, you also get access to the `wt` command, which allows you to launch into the Windows Terminal from anywhere. See all of Windows Terminal's features including adding panes, customizing the font, and more, [here](https://docs.microsoft.com/en-us/windows/terminal/).

Another really popular choice is cmder, which is an extension of a different console emulator called ConEmu (short for console emulator, quite literally). [Cmder](https://cmder.net/) provides a ton of really cool features that inspired Windows Terminal, such as tabs, the ability to add panes, and more. You can even use cmder within the Windows Terminal.

### Cascadia Code [(link)](https://www.youtube.com/watch?v=oHhiMf_6exY)

With all of their recent additions to the developer workflow, Microsoft has also added a new font that works exceptionally well for software development. It's perfect for integration with the Windows Terminal, VS Code, and anywhere else you write code.

### Scott Hanselman's Technical How To's [(link)](https://www.youtube.com/playlist?list=PL0M0zPgJ3HSdI26ZdgX-F8aAKnh9sq6on)

Scott is a Microsoft software engineer, teacher, blogger, and YouTuber. Here's created a wonderful YouTube series detailing how to make the most of Windows 10, especially as a developer. He even has videos on secret Microsoft Word shortcuts, so you can save time on essay writing.

### Fireship's Guide to WSL 2 [(link)](https://www.youtube.com/watch?v=-atblwgc63E)

This YouTube video is a great guide to both explaining and setting up the Windows Subsystem for Linux, in just 10 minutes.

### Mike Robbins' *PowerShell 101* [(link)](https://docs.microsoft.com/en-us/powershell/scripting/learn/ps101/00-introduction?view=powershell-7)

This book goes into a lot of depth, but if you're looking to do something fancy, you'll be able to figure it out with this book. Perhaps the most relevant trick for programmers is creating "aliases", which are abbreviations to execute a certain script. For example, you could type `mdc` and PowerShell would move you into your Documents/ folder.
