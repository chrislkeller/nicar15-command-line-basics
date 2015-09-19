sort
=====

What it does
============

Have you used Excel for sort by ascending/descending order? This is how the command line does it. It works well with deliminated data files, such as csv, or tsv. Use `-r` flag for reverse order.

Examples
========

`-k 2` for the 2nd column

```
$ sort -k 2 zipcode
Adam  12345
Wendy 23456
Bob   34567
Sam   45678
Joe   56789
```