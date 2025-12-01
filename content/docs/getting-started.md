---
weight: 999
title: "Getting Started"
description: "A guide to setting up your computer for C++ development."
icon: "article"
date: "2025-11-30T20:27:46-05:00"
lastmod: "2025-11-30T20:27:46-05:00"
draft: false
toc: true
---
This course relies on a few key pieces of software. Some are crossplatform, like Git and VSCode and others are platform specific. Here I'll walk
you through the installation process for them.

### Common Software
- Git
- VSCode

Git is a [version control system](https://en.wikipedia.org/wiki/Version_control). We use version control to track changes to our code and collaborate with others. 
We'll go into git more in depth at a later date, for now just know that it's a tool we'll use from the command line to share code with each other.

VSCode is an IDE or [Integrated Development Environment](https://en.wikipedia.org/wiki/Integrated_development_environment). We use VSCode to write and debug code. 
It's far from the only editor on the market. I personally use [Neovim](https://neovim.io/) to edit my code and 
[RemedyBG](https://remedybg.itch.io/remedybg) or [RAD Debugger](https://github.com/EpicGamesExt/raddebugger) to debug my code. 
We may look into some of these tools, but for now VSCode will work just fine.

Both git and VSCode have pretty strightforward install steps on every common operating system. On windows you must install git via its dedicated installer
you can find it [here](https://git-scm.com/). On linux you can use the package manager of your choosing. On a debian based system you can use ```sudo apt install git```.

You can download VSCode [here](https://code.visualstudio.com/)


### Windows Specific Software
On windows we rely on microsofts build toold chain, [MSBuild](https://en.wikipedia.org/wiki/MSBuild). To get MSBuild we have to install visual studio. 
You can download it [here](https://visualstudio.microsoft.com/downloads/). Once you start the visual studio installer you must be careful to 
select the correct options on the modules page. Below is a screenshot of this page.

[![msbuild-modify-panel.png](https://i.postimg.cc/zB5GNsD1/msbuild-modify-panel.png)](https://postimg.cc/DWjTdYbC)

Be sure you select the **"Desktop Development with C++"** and **"Game Development with C++"** options.

You'll also need to install the new windows terminal from the windows store. This gives us easy access to a terminal that has all of the build tools configured.

Search for "terminal" in the windows store, you're looking for the entry that looks something like this.

[![windows-terminal.png](https://i.postimg.cc/wMyPGvKf/windows-terminal.png?width=100)](https://postimg.cc/p5vq9PLz)

### Linux Specific Software

Linux is much simpler to get setup. We'll only need to install a few packages using the package manager of your choice, usually your distributions default
package manager will work perfectly fine.

The packages we'll need to install are **clang** and **lldb**. To do this on a debin based distro you would type this into your terminal.

```sudo apt install clang lldb```

Clang is the compiler we'll be using and lldb is the debugger we'll use alongside VSCode.
