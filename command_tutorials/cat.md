cat
===

* Think concatenate
* [Stanford Journalism](http://journalism.stanford.edu/) link for [cat](http://www.compciv.org/unix-tools/#cat)

What it does
============

* Adds the contents of two (or more) files together

Examples
========

* Let's say you have two files: text_1.txt and text_2.txt

    * text_1.txt contains the following:

            I'm just a bill
            Yes, I'm only a bill
            And I'm sitting here on Capitol Hill

    * text_2.txt contains the following:

            Conjunction Junction, what's your function?
            Hooking up two boxcars and making 'em run right.
            Milk and honey, bread and butter, peas and rice.
            Hey that's nice!

    * running cat on these two files will combine their contents and output it to the command line

        * ```cat text_1.txt text_2.txt``` outputs the following to the command line

                I'm just a bill
                Yes, I'm only a bill
                And I'm sitting here on Capitol Hill
                Conjunction Junction, what's your function?
                Hooking up two boxcars and making 'em run right.
                Milk and honey, bread and butter, peas and rice.
                Hey that's nice!

        * ```cat text_1.txt text_2.txt > my_new_file.txt``` will create a new file with the contents of the two files
