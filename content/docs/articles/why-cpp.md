---
weight: 999
title: "Why C++"
description: "Why I still use C++ for game development."
icon: "article"
date: "2025-11-30T19:28:52-05:00"
lastmod: "2025-11-30T19:28:52-05:00"
draft: false
toc: true
---
If you've spent any amount of time on the internet learning about programming or development, you've probably heard something like the following

- C++ is outdated, error prone, and shouldn't be used in new projects.
- C++ is too difficult for new programmers to learn due to its depth and poor error messages.
- C++ is *dangerous*! We can't have new software built with a *dangerous* programming language!

the people writing these claims have good reason to believe them, and they're not entierly wrong on the first and third. C++, especially any standard before C++ 20,
is pretty outdated by modern programming standards. Doing simple things like ```map(x => { doSomething() })``` is difficult and verbose.
This verbosity and difficulty often leads to errors that are hard to track down due to the compiler messages (especially on MSVC) being quite bad. <br>

On the topic of safety:<br> 
I'm not going to sit here and argue that C++ is magically a memory safe language with no bugs. 
What I will argue is that how critical these bugs are is signifiganly reduced by the fact that I am often not writing networked code.
My code almost always lives on one machine that doesnt talk to the outside world at all. If I have a buffer overflow it is incredibly
unlikely that an attacker could find and expoit it to do nefarious things to a customers machine.
Besides, I use asan and valgrind heavily during development. This doesn't mean that I'll catch every memory related bug, but it helps me
catch a majority of them.

On the topic of Modernity:<br>
Newer C++ standards, mainly 20+, are making things like ```map``` a lot less verbose as well as fixing long standing issues like 
[SFINAE](https://en.cppreference.com/w/cpp/language/sfinae.html), 
and [The Static Order Initialization Fiasco.](https://en.cppreference.com/w/cpp/language/siof.html)
Making C++ a much more pleasant language to write. I teach this version of C++. Modern, fast, and reliable.

### **So why do I still use C++ for game development?**
There are a few reasons, some of them good, some of them not so good. The main reason I use and teach C++ is that it is the industry standard
in the game development world and I believe it will continue to be that way for quite some time. I think there are a few contenders to dethrone it
mainly Zig, Odin, and Jai (although I've never actually written a line of the latter). But for the time being C++ isn't going anywhere.
I also know that most of the critical memory safety bugs can be avoided if you simply use some of the tools C++ gives you. ```std::array``` and its siblings
```std::vector```, ```std::string```, and ```std::queue``` cover almost every buffer overflow bug that you commonly encounter.
And smart pointers cover off ownership issues, although I use them rarely and prefer showing explicit ownership at initialization.
Another key reason is that I'd like to actually ship software that uses common API's like Steams API and FMOD without having to write my own bindings.
There are great arguments to use a newer language but C++ is incredibly reliable, used everywhere in the industry, and honestly pretty good if you
take the time to learn what you're doing and spend a little extra time thinking about things like ownership and move semantics.

I won't be switching off of C++ anytime soon, and I don't reccomend you do either.
