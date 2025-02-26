<p align="center">
	<a href="https://gamebanana.com/gamefiles/15309" target="_blank"><img src="/art/FNF Logo.png"></a>
</p>

### This is the repository for Friday Night Funkin: Mic'd Up, previously named FNF: EX Replayability, a non-profit modification of Friday Night Funkin'.

Support the original Newgrounds Build [here](https://www.newgrounds.com/portal/view/770371)!

Play the original build on the [Itch.io page](https://ninja-muffin24.itch.io/funkin)!

Play the Ludum Dare prototype of the original game [here](https://ninja-muffin24.itch.io/friday-night-funkin)!

## Credits / Shoutouts

<p align="right">
<h2>Original Game Creators:</h2>
<h3>🖥 Programmers:</h3>
<a href='https://twitter.com/ninja_muffin99'><b>NinjaMuffin99</b><br><img src="/art/Ninja.png" alt="NinjaMuffin99" width="175" height="175"></a>
<h3>🖼 Artists:</h3>
<b><a href='https://twitter.com/phantomarcade3k'>PhantomArcade3K</a><br>
<a href='https://twitter.com/phantomarcade3k'><img src="/art/Phantom.png" alt="PhantomArcade3K" width="175" height="175"></a><br><br>
<a href='https://twitter.com/evilsk8r'>Evilsk8r</a><br>
<a href='https://twitter.com/evilsk8r'><img src="/art/Evil.png" alt="Evilsk8r" width="175" height="175"></a></b>
<h3>🎶 Musicians:</h3>
<b><a href='https://twitter.com/kawaisprite'>Kawaisprite</a></b><br>
<a href='https://twitter.com/kawaisprite'><img src="/art/Kawai.png" alt="Kawaisprite" width="175" height="175"></a></b>
</p>

<h2>Mod Creators:</h2>
<h3>⚙️ Mod Creator:</h3>
<a href='https://twitter.com/Vershift'><b>Verwex</b><br><img src="/art/Verwex.png" alt="Verwex" width="175" height="175"></a>
<h3>🖥 Additional Programmers:</h3>
<a href='https://twitter.com/kadedeveloper'><b>KadeDev</b><br><img src="/art/Kade.png" alt="KadeDeveloper" width="175" height="175"></a><br><br>
<a href='https://steamcommunity.com/profiles/76561198353865795'><b>Ash237</b><br><img src="/art/Ash.png" alt="Ash237 (temporary link until I find his twitter account)" width="175" height="175"></a>

<p align="center">
	<a href="https://ninja-muffin24.itch.io/funkin"><img src="/art/preloaderArt.png"></a>
</p>

**This mod was made with love to Friday Night Funkin' and its community. Extra love to the team behind it. 💖**

## What can I do with compiling the mod? Why should I compile the mod instead of downloading it from [the Gamabanana page of the mod](https://gamebanana.com/gamefiles/15309)?

Compiling the mod gives access to the `/source` folder, allowing you to change the code of the mod. You can add a lot of cool things with the open source code!

I recommend having a good idea on how to program. Compiling the mod is not for everyone!

If you just want to download and play the mod normally, you can click [here to go to the Gamebanana page of the mod](https://gamebanana.com/gamefiles/15309)!

### **If you do want to compile, continue reading!**

# Installing the Required Programs

<p align="center">
	<a href="https://haxe.org/documentation/introduction/" target="_blank"><img src="/art/haxeLogo.png"></a>
</p>

First you need to install Haxe and HaxeFlixel.
1. [Install Haxe 4.1.5](https://haxe.org/download/version/4.1.5/) (Download 4.1.5 instead of 4.2.0 because 4.2.0 is broken and is not working with gits properly...)
2. [Install HaxeFlixel](https://haxeflixel.com/documentation/install-haxeflixel/) after downloading Haxe

Other installations you will need are the additional libraries. A fully updated list will be in `Project.xml` in the project root. Currently, these are all the things you need to install:
```
flixel
flixel-addons
flixel-ui
hscript
newgrounds
```
So, for each of those type `haxelib install [library]` so shit like `haxelib install newgrounds`.

You will also need to install a couple things that involve Gits. To do this, you need to do a few things first.
1. Download [git-scm](https://git-scm.com/downloads). Works for Windows, Mac, and Linux, just select your build.
2. Follow instructions to install the application properly.
3. Run `haxelib git polymod https://github.com/larsiusprime/polymod.git` to install Polymod.
4. Run `haxelib git discord_rpc https://github.com/Aidan63/linc_discord-rpc` to install Discord RPC.
5. Optional: - Run `haxelib git flixel-addons https://github.com/HaxeFlixel/flixel-addons` to update Flixel-Addons. This fixes the transition bug for zoomed out stage cameras.

You should have everything ready for compiling the mod! Follow the guide below to continue!

# Adding `APIStuff.hx` into `/source`

The API keys of the mod were gitignored so no one could post fake high scores onto the leaderboards in Newgrounds. Unfortunately, because this mod requires the `API` and `EncKey` values to compile, you will need to add a file called `APIStuff.hx` into `/source`.

1. Create a new text file called `APIStuff.hx` inside of the `/source` folder.
2. Copy the following text:
```haxe
package;
class APIStuff
{
	public static var API:String = "";
	public static var EncKey:String = "";
}
```
3. Paste the text into the APIStuff.hx file and save the file.

You should be good from there! Now, onto compiling!

# Compiling the Mod

<p align="center">
	<a href="https://lime-ml.readthedocs.io/en/latest/" target="_blank"><img src="/art/limeLogo.png"></a>
</p>

## HTML Building:

Compiling the mod is rather simple for HTML5 builds.
1. Open your machine's command prompt/terminal and navigate to your root folder of the mod. [An easy guide can be found here!](https://ninjamuffin99.newgrounds.com/news/post/1090480)
2. Type `lime build html5 -debug` to build the HTML5 version of the mod.
3. Type `lime run html5 -debug` to run the HTML5 version of the mod from the command prompt/terminal. (You can also run the mod from `funkin/export/debug/html5/bin`)

You should be all good to play the HTML5 version of the mod!

## Desktop Building:

Desktop building can be a bit tedious. Each different version requires a different setup.

### Linux Building:

1. Open your machine's command prompt/terminal and navigate to your root folder of the mod. [An easy guide can be found here!](https://ninjamuffin99.newgrounds.com/news/post/1090480)
2. Type `lime build linux -debug` to build the Linux version of the mod.
3. Type `lime run linux -debug` to run the Linux version of the mod from the command prompt/terminal. (You can also run the mod from `funkin/export/debug/linux/bin`)

### Mac Building:

1. Open your machine's command prompt/terminal and navigate to your root folder of the mod. [An easy guide can be found here!](https://ninjamuffin99.newgrounds.com/news/post/1090480)
2. Type `lime build mac -debug` to build the Mac version of the mod.
3. Type `lime run mac -debug` to run the Mac version of the mod from the command prompt/terminal. (You can also run the mod from `funkin/export/debug/mac/bin`)

### Windows Building:
**THIS METHOD REQUIRES AROUND 22 GIGABYTES OF STORAGE.**
1. Install [Visual Studio Community 2019](https://visualstudio.microsoft.com/downloads/).
2. Open the installer and go to the individual workloads tab and download the following:
```
* C++ CMake tools for windows 
* C++ Profiling tools 
* C++ ATL for v142 build tools (x86 & x64)
* C++ MFC for v142 build tools (x86 & x64)
* C++/CLI support for v142 build tools (14.21)
* C++ Modules for v142 build tools (x64/x86)
* Clang Compiler for Windows
* MSVC v140 - VS 2015 C++ build tools (v14.00) 
* MSVC v141 - VS 2017 C++ x64/x86 build tools
* MSVC v142 - VS 2019 C++ x64/x86 build tools
* Windows 10 SDK (10.0.16299.0)
* Windows 10 SDK (10.0.17134.0)
* Windows SDK (10.0.17763.0)
```
3. Wait for the install to finish, which might take a while.
4. Open your machine's command prompt/terminal and navigate to your root folder of the mod. [An easy guide can be found here!](https://ninjamuffin99.newgrounds.com/news/post/1090480)
5. Once everything is installed, type `lime build windows -debug` to build the windows version of the mod.
6. Type `lime run windows -debug` after the mod is compiled to run the windows version of the mod. (You can also run the mod from `funkin/export/debug/windows/bin`)

# All done!
You should have been able to compile the whole mod now! What can you do now? Well, you can mod to your heart's desire! Since this mod is open source, the creator loves seeing what other talented artists and programmers can make!
Special thanks to the amazing group of dedicated people that are making the original game amazing, and the modding teak for making this mod possible!

<p align="center">
	💖💖
</p>