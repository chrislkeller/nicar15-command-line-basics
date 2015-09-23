#ONA15 Workshop Walkthrough
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

        ```$ mkdir my_ona_data```

* [cd](http://www.compciv.org/unix-tools/#cd): change directory

    * Let's move - or change - into that directory

        ```$ cd my_ona_data```

    * ```cd ..``` allows us to move back one level
    * ```cd ../..``` allows us to move back two levels

* [touch](http://www.compciv.org/unix-tools/#touch): update a file's timestamp, or create a new file

    * Let's make a new file. We're not going to do much with it, but hey - you can make a new file from the command line

        ```$ touch my_ona_file.txt```

* [curl](http://www.compciv.org/unix-tools/#curl): transfer content from a URL

    * Now we're getting somewhere. Let's download some data. This is data from the Pipeline and Hazardous Materials Safety Administration on oil and natural gas pipeline operators that was compiled via a [web scraper](https://github.com/SCPR/kpcc-data-team/tree/master/tools-and-scripts/pull-us-pipeline-operators) written by [Will Craft](https://twitter.com/craftworksxyz).

     The real file exists at ```https://github.com/chrislkeller/nicar15-command-line-basics/blob/master/ONA15/phmsa_pipeline_data.zip?raw=true```. I saved a copy [here](https://s3-us-west-1.amazonaws.com/dataona/phmsa_pipeline_data.zip > phmsa_pipeline_data.zip) that we can access.

        ```$ curl https://s3-us-west-1.amazonaws.com/dataona/phmsa_pipeline_data.zip > phmsa_pipeline_data.zip```

* [unzip](http://www.compciv.org/unix-tools/#unzip): extract data from a zip file

    * We can unzip this zip file from the command line

        ```$ unzip phmsa_pipeline_data.zip```

* [cd](http://www.compciv.org/unix-tools/#cd): change directory

    * Let's move - or change - into that directory

        ```$ cd phmsa_pipeline_data```

* [ls](http://www.compciv.org/unix-tools/#ls): list files in a specified directory

    * Let's see what exists in current directory

        ```$ ls```

* [head](http://www.compciv.org/unix-tools/#head): (-n) display the first n lines of a file

    * See the first 10 lines of ```phmsa_pipeline_operators.csv```

        ```$ head -n 10 phmsa_pipeline_operators.csv```

* [tail](http://www.compciv.org/unix-tools/#tail): (-n) display the last n lines of a file

    * See the last five lines of ```phmsa-incident-details.csv```

        ```$ tail -n 5 phmsa-incident-details.csv```

* [cp](http://www.compciv.org/unix-tools/#cp): make a duplicate of a file

        ```$ cp phmsa-incident-details.csv incidents_to_explore.csv```

* [mv](http://www.compciv.org/unix-tools/#mv): move a file to a new directory, or simply rename it

    * In this case we're not necessarily "moving" the file, but in renaming it we're moving it to a new location for the file system

        ```$ mv incidents_to_explore.csv my_new_incidents_to_explore.csv```

    * Let's name it back to what it was

        ```$ mv my_new_incidents_to_explore.csv incidents_to_explore.csv```

* [grep](http://www.compciv.org/unix-tools/#grep): globally search a regular expression and print

    * Let's see how many times the name CITGO appears in the file.

        ```$ grep "RUPTURED" incidents_to_explore.csv```

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

    * Let's make a new file incidents involving *Phillips 66 Pipeline* and then combine it with our ```buckeye_partners.csv```

        ```$ grep "Phillips 66 Pipeline" incidents_to_explore.csv > phillips_66_pipeline.csv```

        ```$ cat buckeye_partners.csv phillips_66_pipeline.csv```

        ```$ cat buckeye_partners.csv phillips_66_pipeline.csv > target_data.csv```
