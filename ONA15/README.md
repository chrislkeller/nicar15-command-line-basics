#ONA15 Workshop Walkthrough
=============================

![](/ONA15/ONA_15_Session_Cover_Slide.png)

## Navigate with CLI

* [pwd](http://www.compciv.org/unix-tools/#pwd): print working directory

    * Let's see where we are in the file system

        ```$ pwd```

* [man](http://www.compciv.org/unix-tools/#man): search the manual or "how to" for a particular command

    * Now's a good time to introduce ```man``` or manual. Let's see what ```pwd``` does

        ```$ man pwd```

    * Use arrow keys to read on. To exit the manual, hit ```q``` (for quit)

    * If you can't find help with ```man```, try ```info``` or add a ```-?``` or ```--help``` argument on the command

        ```$ info pwd```
        ```$ pwd -?```
        ```$ pwd --help```

* [ls](http://www.compciv.org/unix-tools/#ls): list files in a specified directory

    * Let's see what exists in current directory

        ```$ ls```

* [cd](http://www.compciv.org/unix-tools/#cd): change directory

    * Let's move - or change - into Desktop. When you create, edit directories and files you can see it reflected on your Desktop.

        ```$ cd Desktop```

    * ```cd ..``` allows us to move up one level (parent directory)
    * ```cd ../..``` allows us to move back two levels (grandparent)

## Create directories and files

* [mkdir](http://www.compciv.org/unix-tools/#mkdir): make directory

    * We'll make a new directory to store some files in

        ```$ mkdir my_ona_data```

    * Use a command above to go to `my_ona_data`. Do you remember which one it is?


* [touch](http://www.compciv.org/unix-tools/#touch): update a file's timestamp, or create a new file

    * Once you've navigated to `my_ona_data`, let's make a new file. We're not going to do much with it, but hey - you can make a new file from the command line

        ```$ touch my_ona_file.txt```

    * Now use a command above to check what's in the directory. Cool, eh?

## Let's get some data!

* [curl](http://www.compciv.org/unix-tools/#curl): transfer content from a URL

    * Now we're getting somewhere. Let's download some data. **This is data from the Pipeline and Hazardous Materials Safety Administration on oil and natural gas pipeline operators** that was compiled via a [web scraper](https://github.com/SCPR/kpcc-data-team/tree/master/tools-and-scripts/pull-us-pipeline-operators) written by [Will Craft](https://twitter.com/craftworksxyz).

     The real file exists at ```https://github.com/chrislkeller/nicar15-command-line-basics/blob/master/ONA15/phmsa_pipeline_data.zip?raw=true```. I saved a copy [here](https://s3-us-west-1.amazonaws.com/dataona/phmsa_pipeline_data.zip > phmsa_pipeline_data.zip) that we can access.

        ```$ curl https://s3-us-west-1.amazonaws.com/dataona/phmsa_pipeline_data.zip > phmsa_pipeline_data.zip```

* [ls](http://www.compciv.org/unix-tools/#ls): list files in a specified directory

    * Let's see what exists in current directory

        ```$ ls```

* [unzip](http://www.compciv.org/unix-tools/#unzip): extract data from a zip file

    * We can unzip this zip file from the command line

        ```$ unzip phmsa_pipeline_data.zip```

* [ls](http://www.compciv.org/unix-tools/#ls): list files in a specified directory

    * Let's see what exists in current directory

        ```$ ls```

* [cd](http://www.compciv.org/unix-tools/#cd): change directory

    * Let's move - or change - into that directory. The directory name is complicated. To make life easier, CLI allows you to autocomplete once you give it a letter/a few letters. Try this:

        ```$ cd ph``` (then instead return, hit tab)

    * The directory is spelt out for you!

        ```$ cd pphmsa_pipeline_data``` (now hit return)

* What's the next command to use here to see what is in the directory? Hint: you've used it at least three times now.

## Exploring data

* What's your usual workflow when you working with a csv file?

* [head](http://www.compciv.org/unix-tools/#head): (-n) display the first n lines of a file

    * See the first 10 lines of ```phmsa_pipeline_operators.csv``` Don't forget to use tab for autocomplete.

        ```$ head -n 10 phmsa_pipeline_operators.csv```

* [tail](http://www.compciv.org/unix-tools/#tail): (-n) display the last n lines of a file

    * See the last five lines of ```phmsa-incident-details.csv```

        ```$ tail -n 5 phmsa-incident-details.csv```

* [cp](http://www.compciv.org/unix-tools/#cp): make a duplicate of a file

    * We never want to work with our original data so let's make copies of each file

        ```$ cp phmsa_pipeline_operators.csv BAK_phmsa_pipeline_operators.csv```
        ```$ cp phmsa-incident-details.csv BAK_phmsa-incident-details.csv```

* [mv](http://www.compciv.org/unix-tools/#mv): move a file to a new directory, or simply rename it

    * In this case we're not necessarily "moving" the file, but in renaming it we're moving it to a new location for the file system

        ```$ mv phmsa-incident-details.csv incidents_to_explore.csv```

* [grep](http://www.compciv.org/unix-tools/#grep): globally search a regular expression and print

    * Let's see how many times the term RUPTURE appears in the file.

        ```$ grep "RUPTURE" incidents_to_explore.csv```

    * Grepping multiple files for case insensitive term, showing file names with the match

        ```$ grep -i "Buckeye Partners" incidents_to_explore.csv phmsa_pipeline_operators.csv```

    * Let's create a new file with only the incidents from Buckeye Partners

        ```$ grep "Buckeye Partners" incidents_to_explore.csv > buckeye_partners.csv```

* [sort](http://www.compciv.org/unix-tools/#sort): sort lines of text from a file

    * Let's sort the text file by the City Name

        ```$ sort -k 4 -t "," buckeye_partners.csv```

    * Let's sort the text file by the State Name

        ```$ sort -k 6 -t "," buckeye_partners.csv```

    * Let's reverse the sort order by the State Name

        ```$ sort -r -k 6 -t "," buckeye_partners.csv```

* [cat](http://www.compciv.org/unix-tools/#cat): concatenate, or combine two or more files

    * Let's make a new file incidents involving *Phillips 66 Pipeline* and then combine it with our ```buckeye_partners.csv``` that contains incidents with *Buckeye Partners*

        ```$ grep "Phillips 66 Pipeline" incidents_to_explore.csv > phillips_66_pipeline.csv```

        ```$ cat buckeye_partners.csv phillips_66_pipeline.csv```

        ```$ cat buckeye_partners.csv phillips_66_pipeline.csv > target_data.csv```
