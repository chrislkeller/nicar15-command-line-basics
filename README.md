How I learned to take command of the command line: A journalists guide to getting started
=========================================================================================

* [What Is The Command Line Anyway](#what-is-the-command-line-anyway)
* [On The Computer](#on-the-computer)
* [Getting Started](#getting-started)
* [Where Do You Go From Here](#where-do-you-go-from-here)
* [Learning More, Reference And Tools](#learning-more-reference-and-tools)
* [About Us](#about-us)


What Is The Command Line Anyway
===============================

....


On The Computer
===============

This #NICAR15 hands-on session aims to help beginners learn some basic commands in the command line interface (CLI) that can help them every day, including navigating through directories, creating files and tools to look at and work with structured data. If you're familiar with grep and curl this will likely be review. We'll end by highlighting some command line libraries that are musts for reporters, and provide additional resources so participants can go deeper on their own.

* On your computer:
	* If you're using Mac OS or Linux you'll be OK with the standard terminal application.
		* On Mac OS click on the spotlight search on the topright of your screen, type "terminal" and open the CLI.
			* Many Mac OS users use an application called [iTerm2](http://iterm2.com/) which offers additonal features.
		* On Linux...
	* On a Windows machine you can open the CLI by opening the Start Menu and clicking the Run item. In the box that appears, type the letters cmd. This should open up your CLI.
		* Windows users also have the option of installing [Cygwin](https://www.cygwin.com/) which brings the Unix CLI to Windows. You will want to make sure that [curl is installed](https://stackoverflow.com/questions/3647569/how-do-i-install-curl-on-cygwin).
		* On a Windows machine you can also install [VirtualBox](https://www.virtualbox.org/) and [Vagrant](https://www.vagrantup.com/) to get an *nix machine up and running. That is beyond the scope of this session.


Getting Started
===============

## Keyboard shortcuts are awesome

* tab completion
* ctrl + a and ctrl + e

## On to the commands

* [cd](#): **c**hange **d**irectory
* [ls](#): **l**i**s**t files
	* list all the content in the current directory
* [mkdir](#): **m**a**k**e **d**irectory
	* make a directory within the current directory
* [touch](#):
	* create a file within the current directory
* [pwd](http://cli.learncodethehardway.org/book/ex2.html): **p**rint **w**orking **d**irectory
* [grep](http://cli.learncodethehardway.org/book/ex18.html): **g**lobally search a **r**egular **e**xpression and **p**rint
* [cat](http://cli.learncodethehardway.org/book/ex13.html):
* [head](#):
* [tail](#): (-n) display the last n lines of a file
* [curl](#):
* [sort](#):
* [man](#): search the online **man**ual for a particular command


Where Do You Go From Here
=========================

Many of the commands we detailed in this session represent the basics, some of the foundational sorts of things you can do to begin to be proficient. But there are many more, and a [discussion post-#NICAR14](https://twitter.com/mikejcorey/status/440159788979077121) highlighted many of them. They include:

* [sudo](https://xkcd.com/149/)
* [env vars](http://cli.learncodethehardway.org/book/ex21.html)
* [ack](http://beyondgrep.com/)
* [sed](http://www.grymoire.com/Unix/sed.html)
* [cut](http://www.thegeekstuff.com/2013/06/cut-command-examples/)
* [\>](http://cli.learncodethehardway.org/book/ex15.html)
* [|](http://cli.learncodethehardway.org/book/ex15.html)
* [vim](http://www.vim.org/)
* [tr](https://en.wikipedia.org/wiki/Tr_%28Unix%29)
* [iconv](https://en.wikipedia.org/wiki/Iconv)
* [xargs](https://en.wikipedia.org/wiki/Xargs)
https://en.wikipedia.org/wiki/Xargs


Learning More, Reference And Tools
==================================

## Learning More

* Noah Veltman's [The Command Line Murders: Teaching the Terminal with a Detective Noir](http://veltman.tumblr.com/post/65613277843/the-command-line-murders-teaching-the-terminal-with-a)
* [Over the wire terminal game](http://overthewire.org/wargames/bandit/bandit0.html)
* [Terminus game](http://web.mit.edu/mprat/Public/web/Terminus/Web/main.html)

## Reference

* [Linux Command-Line Cheat Sheet](http://www.computerworld.com/s/article/print/9030259/Linux_Command_Line_Cheat_Sheet)
* [Basics of Getting Around](https://github.com/amandabee/cunyjdata/blob/master/assignments/commandline.md)
* [UNIX tricks](http://cfenollosa.com/misc/tricks.txt)
* [Command Line Fu](http://www.commandlinefu.com/commands/browse/sort-by-votes)
* [Useful Unix commands for exploring data](http://datavu.blogspot.com/2014/08/useful-unix-commands-for-exploring-data.html)
* [Advanced command line tricks using json and XML and CSVs](http://jeroenjanssens.com/2013/09/19/seven-command-line-tools-for-data-science.html)

## Tools

* [csvkit](http://csvkit.readthedocs.org/en/latest/index.html):
* [csv de dupe](https://github.com/datamade/csvdedupe):
* homebrew


About Us
========

* Jue Yang
	* Xxxxx
* AJ Vicens
	* Xxxxx
* Chris Keller
	* Xxxxx
