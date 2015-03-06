How I learned to take command of the command line: A journalists guide to getting started
=========================================================================================

* [Getting To Know You](#getting-to-know-you)
* [What Is The Command Line Anyway](#what-is-the-command-line-anyway)
* [Getting Started](#getting-started)
* [Where Do You Go From Here](#where-do-you-go-from-here)
* [Learning More, Reference And Tools](#learning-more-reference-and-tools)
* [About Us](#about-us)

Getting To Know You
===================

Let's zip around the room to get an idea of who you are, what you do and what you want to learn

What Is The Command Line Anyway
===============================

An alternative to accessing files and opening directories and files through a graphical user interface. Oh, and there are some fun tools there too.

Getting Started
===============

## What we're going to do

This #NICAR15 hands-on session aims to help beginners learn some basic commands in the command line interface (CLI) that can help them every day, including navigating through directories, creating files and tools to look at and work with structured data. If you're familiar with grep and curl this will likely be review. We'll end by highlighting some command line libraries that are musts for reporters, and provide additional resources so participants can go deeper on their own.

## On your computer:

* If you're using Mac OS or Linux you'll be OK with the standard terminal application.
	* On Mac OS click on the spotlight search on the topright of your screen, type "terminal" and open the CLI.
		* Many Mac OS users use an application called [iTerm2](http://iterm2.com/) which offers additonal features.
	* On a Windows machine you can open the CLI by opening the Start Menu and clicking the Run item. In the box that appears, type the letters cmd. This should open up your CLI.
		* Windows users also have the option of installing [Cygwin](https://www.cygwin.com/) which brings the Unix CLI to Windows. You will want to make sure that [curl is installed](https://stackoverflow.com/questions/3647569/how-do-i-install-curl-on-cygwin).
		* On a Windows machine you can also install [VirtualBox](https://www.virtualbox.org/) and [Vagrant](https://www.vagrantup.com/) to get an *nix machine up and running. That is beyond the scope of this session.

## Keyboard shortcuts are awesome

* tab completion: use to finish command, directory or file names, or to see directories or files that match
* ctrl + a: move to the beginning of a line
* ctrl + e: move to the end of a line
* ctrl + c: terminate a command that is running
* up arrow: cycle back through previous commands

## UNIX features you should know

* redirection - [\>](http://cli.learncodethehardway.org/book/ex15.html)
	* Take the output of a file and create a new file with it
* append - [\>>](#)
	* .....
* piping - [|](http://cli.learncodethehardway.org/book/ex15.html)
	* .....

## On to the workshop

* [ls](http://www.compciv.org/unix-tools/#ls): list files in a specified directory

	* Xxxx xxxx

		```$ ls```

* [mkdir](http://www.compciv.org/unix-tools/#mkdir): make directory

	* Xxxx xxxx

		```$ mkdir my_nicar_data```

* [cd](http://www.compciv.org/unix-tools/#cd): change directory

	* Xxxx xxxx

		```$ cd my_nicar_data```

* [pwd](http://www.compciv.org/unix-tools/#pwd): print working directory

	* Xxxx xxxx

		```$ pwd```

* [touch](http://www.compciv.org/unix-tools/#touch): update a file's timestamp, or create a new file

	* Xxxx xxxx

		```$ touch my_new_file.txt```

* [curl](http://www.compciv.org/unix-tools/#curl): transfer content from a URL

	* Download crime data from the Atlanta Police Department
	
		```$ curl http://www.atlantapd.org/pdf/crime-data-downloads/D4314587-D61E-4B4F-9C4C-7CBA29B334F5.zip > my_crime_data_file.zip```

* [unzip](#): extract data from a zip file

	* Xxxx xxxx 

		```$ unzip my_crime_data_file.zip```

* [mv](#): move a file to a new directory, or simply rename it

	* Xxxx xxxx

		```$ mv COBRA022715.txt atlanta-crime-2009-2015.txt```

* [head](http://www.compciv.org/unix-tools/#head): (-n) display the first n lines of a file

	* See the first five lines of the text file, including the header file.

		```$ head n -5 atlanta-crime-2009-2015.txt```

* [tail](http://www.compciv.org/unix-tools/#tail): (-n) display the last n lines of a file

	* See the last five lines of the text file, including the header file.

		```$ tail n -5 atlanta-crime-2009-2015.txt```

* [cat](http://www.compciv.org/unix-tools/#cat): concatenate, or combine two or more files

	* Output each row and find out how many rows you have in this dataset.

		```$ cat atlanta-crime-2009-2015.txt```

* [grep](http://www.compciv.org/unix-tools/#grep): globally search a regular expression and print

	* Start looking at only larceny crimes.

		```$ grep "LARCENY" atlanta-crime-2009-2015.txt > larceny.txt``` 

* [sort](http://www.compciv.org/unix-tools/#sort): sort lines of text from a file

	* Let's sort the text file by the MI_PRINX

		```$ sort larceny.txt```

	* Let's reverse the sort order

		```$ sort -r larceny.txt```

* [man](http://www.compciv.org/unix-tools/#man): search the manual or "how to" for a particular command

Where Do You Go From Here
=========================

**Get the idea? Go explore!!!**

Many of the commands we detailed in this session represent the basics, some of the foundational sorts of things you can do to begin to be proficient. But there are many more, and a [discussion post-#NICAR14](https://twitter.com/mikejcorey/status/440159788979077121) highlighted many of them. They include:

* [sudo](https://xkcd.com/149/)
* [tr](http://www.compciv.org/unix-tools/#tr)
* [iconv](https://en.wikipedia.org/wiki/Iconv)
* [wc](http://www.compciv.org/unix-tools/#wc)
* [mv](http://www.compciv.org/unix-tools/#mv)
* [ack](http://beyondgrep.com/)
* [sed](http://www.grymoire.com/Unix/sed.html)
* [cut](http://www.thegeekstuff.com/2013/06/cut-command-examples/)
* [vim](http://www.vim.org/)
* [env vars](http://cli.learncodethehardway.org/book/ex21.html)
* [xargs](https://en.wikipedia.org/wiki/Xargs)

Learning More, Reference And Tools
==================================

## Learning More

* Noah Veltman's [The Command Line Murders: Teaching the Terminal with a Detective Noir](http://veltman.tumblr.com/post/65613277843/the-command-line-murders-teaching-the-terminal-with-a)
* [Over the wire terminal game](http://overthewire.org/wargames/bandit/bandit0.html)
* [Terminus game](http://web.mit.edu/mprat/Public/web/Terminus/Web/main.html)

## Reference

* [The Command Line Crash Course](http://cli.learncodethehardway.org/book/)
* [Unix tools](http://www.compciv.org/unix-tools/)
* [UNIX tricks](http://cfenollosa.com/misc/tricks.txt)
* [Working With CSVs On The Command Line](http://bconnelly.net/working-with-csvs-on-the-command-line/)
* [Linux Command-Line Cheat Sheet](http://www.computerworld.com/s/article/print/9030259/Linux_Command_Line_Cheat_Sheet)
* [Basics of Getting Around](https://github.com/amandabee/cunyjdata/blob/master/assignments/commandline.md)
* [Command Line Fu](http://www.commandlinefu.com/commands/browse/sort-by-votes)
* [Unix commands for exploring data](http://datavu.blogspot.com/2014/08/useful-unix-commands-for-exploring-data.html)
* [Advanced command line tricks using json and XML and CSVs](http://jeroenjanssens.com/2013/09/19/seven-command-line-tools-for-data-science.html)

## Tools

* [csvkit](http://csvkit.readthedocs.org/en/latest/index.html):
	* *"a suite of utilities for converting to and working with CSV, the king of tabular file formats."*
	* [Getting it installed](https://github.com/amandabee/cunyjdata/wiki/Tutorial:-Installing-CSVKit) if `pip install csvkit` doesn't sound persuasive
	* Using it to trim NYC DOB complaint records down to a manageable size [tutorial](https://github.com/amandabee/cunyjdata/wiki/Tutorial:-CSVkit)
	* Using it to trim NYC's City Planning data down a ton [notes](https://github.com/amandabee/cunyjdata/blob/master/lecture%20notes/csvkit.md)

* [csv de dupe](https://github.com/datamade/csvdedupe):
* [homebrew](http://brew.sh/)

About Us
========

* AJ Vicens
	* Mother Jones
* Chris Keller
	* Data editor and news applications developer at KPCC, the NPR affiliate in Pasadena, Calif. Chris joined KPCC in 2012 after spending more than 15 years in various print and digital roles at newspapers of various sizes in the Midwest.
	* [GitHub](https://github.com/chrislkeller)
	* [@ChrisLKeller](https://twitter.com/chrislkeller)
* Jue Yang
    * Technologist at CUNY Graduate School of Journalism in New York. Jue is a designveloper. (Unfortunately due to major snowfall, Jue's flight to NICAR was cancelled. She couldn't join NICAR in person this year, but will be virtually available should you have any questions!)
    * [GitHub](https://github.com/jueyang)
    * [@jue_yang](https://twitter.com/jue_yang)
