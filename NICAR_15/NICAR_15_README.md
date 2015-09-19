#NICAR15 Workshop Walkthrough
=============================

* [pwd](http://www.compciv.org/unix-tools/#pwd): print working directory

    * Let's see where we are in the file system

        ```$ pwd```

* [man](http://www.compciv.org/unix-tools/#man): search the manual or "how to" for a particular command

    * Now's a good time to introduce ```man``` or manual. Let's see what ```pwd``` does

        ```$ man pwd```

    * If you can't find help with ```man```, try ```info``` or add a ```-?``` or ```--help``` argument on the command

        ```$ info pwd```
        ```$ pwd -?```
        ```$ pwd --help```

* [ls](http://www.compciv.org/unix-tools/#ls): list files in a specified directory

    * Let's see what exists in current directory

        ```$ ls```

* [mkdir](http://www.compciv.org/unix-tools/#mkdir): make directory

    * We'll make a new directory to store some files in

        ```$ mkdir my_nicar_data```

* [cd](http://www.compciv.org/unix-tools/#cd): change directory

    * Let's move - or change - into that directory

        ```$ cd my_nicar_data```

    * ```cd ..``` allows us to move back one level
    * ```cd ../..``` allows us to move back two levels

* [touch](http://www.compciv.org/unix-tools/#touch): update a file's timestamp, or create a new file

    * Let's make a new file. We're not going to do much with it, but hey - you can make a new file from the command line

        ```$ touch my_new_file.txt```

* [curl](http://www.compciv.org/unix-tools/#curl): transfer content from a URL

    * Now we're getting somewhere. Let's download crime data from the Atlanta Police Department. The real file exists at ```http://www.atlantapd.org/pdf/crime-data-downloads/D4314587-D61E-4B4F-9C4C-7CBA29B334F5.zip```. I saved a copy here that we can access.

        ```$ curl https://s3.amazonaws.com/datanicar/atlanta_pd_crime_data_file.zip > my_atlanta_crime_data_file.zip```

* [unzip](http://www.compciv.org/unix-tools/#unzip): extract data from a zip file

    * We can unzip this zip file from the command line

        ```$ unzip my_atlanta_crime_data_file.zip```

* [mv](http://www.compciv.org/unix-tools/#mv): move a file to a new directory, or simply rename it

    * In this case we're not necessarily "moving" the file, but in renaming it we're moving it to a new location for the file system

        ```$ mv COBRA022715.txt atlanta-crime-2009-2015.txt```

* [head](http://www.compciv.org/unix-tools/#head): (-n) display the first n lines of a file

    * See the first five lines of the text file, including the header file.

        ```$ head -n 5 atlanta-crime-2009-2015.txt```

* [tail](http://www.compciv.org/unix-tools/#tail): (-n) display the last n lines of a file

    * See the last five lines of the text file, including the header file.

        ```$ tail -n 5 atlanta-crime-2009-2015.txt```

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
