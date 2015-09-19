cURL
=====

* Think transfer a URL
* [Stanford Journalism](http://journalism.stanford.edu/) link for [cat](http://www.compciv.org/unix-tools/#curl)
* curl [manual and options](http://curl.haxx.se/docs/manpage.html)

What it does
============

curl is a tool to transfer data from or to a server

Examples
========

* Retrieve the data at the URL and print to standard output.

        curl https://www.fdic.gov/bank/individual/failed/banklist.csv

* Retrieve the data at the URL and save standard output as a file name

        curl https://www.fdic.gov/bank/individual/failed/banklist.csv -o bank_list.csv

* Fetch only the headers from from a website

        curl https://www.fdic.gov/bank/individual/failed/banklist.csv --head
