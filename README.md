Pdfc --  PDF Compressor
=======================

Original Author: Sylvain Carlioz, 6/03/2017

Simple python wrapper script to use ghoscript function to compress PDF files.
With this class you can compress and or fix a folder with (corrupt) PDF files.

You can also use this class within your own scripts just do a
import CompressPDF

Installation
-------------
* Install dependency Ghostscript.
On MacOSX: `brew install ghostscript`
On Windows: install binaries via [official website] (https://www.ghostscript.com/)
* Create a symbolic link if you want to run it everywhere in bash
`ln -s pdf_creator.py pdfc`
* Add in PATH environment variable
On MacOSX:
`echo export=/absolute/path/of/the/folder/script/:$PATH >> ~/.bash_profile`

Usage
-----
`pdfc [-sf startFolder] [-cl compressLevel] [-s showInfo]`

Ex:
`pdfc -sf /User/Me/PDF-Files/ -cd 2 -s 1`

Output Example:
```
Compress PDF...
Compression by 65%.
Final file size is 1.4MB
Done.
```



Options
-------
* `-c` or `--compress` specifies 5 levels of compression, similar to standard pdf generator level:
  * 0: default
  * 1: prepress
  * 2: printer
  * 3: ebook
  * 4: screen
* `-o`or `--out` specifies the output file path. If not specified, input file will be erased.
