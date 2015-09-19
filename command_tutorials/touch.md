touch
=====

* Update a file's access date/time and/or modification date/time, or creates the file if it doesn't exist
* [Stanford Journalism](http://journalism.stanford.edu/) link for [cat](http://www.compciv.org/unix-tools/#touch)

What it does
============

```touch``` updates a file's access date/time and/or modification date/time. If the file does not exist, ```touch``` effectively creates a new, empty file to work with. This latter example is the use case many in the journalism world use frequently.

> ["Touch eliminates the unnecessary steps of opening the file, saving the file, and closing the file again. Instead it simply updates the dates associated with the file or directory."](https://en.wikipedia.org/wiki/Touch_%28Unix%29)

Examples
========

* To create a file if it doesn't exist

        touch my_new_file.txt

* To update a file's access date/time and/or modification date/time if it does exist

        touch my_file.txt
