<p align="center"><img src="https://i.imgur.com/kc9EMv1.png"></p>

# Description
A light configuration to give a little style and accessories to the windows terminal

**This guide is practically a copy and paste from "Anup Aglawe" guide you can see this at the end of this repository in the credits section**

---
# Requirements
* Install windows terminal via [microsoft store](https://www.microsoft.com/p/windows-terminal/9n0dx20hk701?rtc=1&activetab=pivot:overviewtab) or via [chocolatey](https://chocolatey.org/) <code>choco install microsoft-windows-terminal</code>
* Open windows powershell and install the following modules (they will allow us to use special icons from the font) <pre>Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser</pre>
<b>(optional) (This other module will allow us to color text, it is in case we want to make a welcome message that will be displayed every time we start the terminal)</b><pre>Install-Module -Name PSWriteColor</pre>
* In order for the icons to load properly we need a patched font, I personally use [LiterationMono Nerd Font](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/LiberationMono.zip) but you could use any font from [nerd fonts](https://www.nerdfonts.com/) (if this is the case, you need to change this line of code from settings.json to use whatever font you want)
<code>"fontFace": "name of the font",</code>

---
# Configuration
## Important, if you are going to copy something from this configuration you will have to replace all the "guid" with yours

Now you have to enter the configuration file of windows terminal. The easiest way is opening it from the menu 
<p align="center"><img src="https://i.imgur.com/5jrdSVG.png"></p>
or if that doesn't work you can try going to this route (which is probably not the same)

<pre>C:\Users\ttuna\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState</pre>
Now what remains would be to replace certain fields with your custom settings

For example:

<code>"guid": "{guid1}",</code> with your personal guid1

<code>"guid": "{guid2}",</code> with your personal guid1

<code>"guid": "{guid3}",</code> with your personal guid1

<code>"name": "EXAMPLENAME",</code> with a name that you want to give your terminal

<code>"icon": "C:\\PATH\\TO\\YOUR\\ICON",</code> path to an icon that you want to put

<code>"backgroundImage": "C:\\PATH\\TO\\YOUR\\BACKGROUNDIMAGE",</code> path to an background image that you want to put

<code>"startingDirectory": "C:\\PATH\\TO\\YOUR\\STARTINGDIRECTORY"</code> path in which the terminal is going to start

And that would be the whole terminal part, for the powershell it is easy, just replace the settings that should have been created in the following path
<pre>C:\Users\ttuna\Documents\WindowsPowerShell</pre>

now test that everything works correctly, if you get a problem with the scripts do the following 
open a powershell with administrator permissions and run the following code:
<pre>Set-ExecutionPolicy RemoteSigned -Force</pre>

now press windows key + r or just type "Run Program Or File" and run the following code
<code>gpedit.msc</code>

that would have to open a window, then follow the next steps (sorry if it's in spanish)

<p align="left"><img src="https://i.imgur.com/lQzreuu.png"></p>
<p align="left"><img src="https://i.imgur.com/hbTnQMB.png"></p>
<p align="left"><img src="https://i.imgur.com/SjkibiD.png"></p>

### My configuration
Personally most of the time I use the terminal with [vim](https://www.vim.org/), that's why I have some changed keyboard shortcuts, you can configure your own in the [settings.json](https://github.com/enzoarguello512/windows-terminal-config/blob/main/settings.json) file to get the maximum potential from the terminal, more info [here](https://aka.ms/terminal-keybindings), mine are the following:

* Ctrl+Shift+C to copy

line:

<code>{ "command": {"action": "copy", "singleLine": false }, "keys": "ctrl+shift+c" },</code>

* Ctrl+Shift+V to paste

line:
        
<code>{ "command": "paste", "keys": "ctrl+shift+v" },</code>

---
# Credits
* [Anup Aglawe](https://dev.to/anupa/beautify-your-windows-terminal-1la8)
* to the owners of the image
