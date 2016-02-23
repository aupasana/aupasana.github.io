---
layout: page
title: Software
toc: true
---

## Mudgala Kosha

The mudgala koṣa is an application that searches several skt-eng / eng-skt dictionaries. It will search an offline version of the monier-williams dictionary, and several online dictionaries including the Apte dictionary. It also integrates with several online tools including the INRIA sanskrit reader, and JNU declension engine. It accepts several input methods (including itrans, baraha, harvard), and can output sanskrit text in a variety of scripts.

Todo: add github repo and place link here

## Mudgala IME

This is a windows-only input method editor and conversion utility to convert between various transliteration and unicode output formats. There are other stand-alone IMEs, such as the google IME, and other stand-alone convertors. In spite of that, for some use cases, this tool is superior to other tools.

To use this tool, download and unzip the file. Run the mudgala-ime exe file, and chose your input and output scripts. Use the button in the window to do the conversion in the window. Use the F11 button as a toggle to type directly in unicode aware apps such as Microsoft word.

Todo: add new github repo and place link here

## Mudgala Hora

This software was a research project into jyotish computational methods. Most people should not use this, as they would benefit from the jagannatha hora software, which is much more advanced. Since the mudgala hora software is released under the GPL, it may still be of some use, and the sources are available here.

Todo: add new github repo and place link here

## Lipika IME

On a Mac, use [LipikaIME][] for transliteration based input in Indian languages. Though it supports Itrans mappings, it does not include popular mappings used in software such as Itranslator (eg. 'M'), or multiple character output for sequences such as 'x' and 'GY'. The two files below have a complete set of Itrans mappings, along with the ability to typeset vedic accents, and independent vowels.

* Replace "/Library/Input Methods/LipikaIME.app/Contents/Resources/Schemes/Transliteration/ITRANS.tlr" with this updated [ITRANS.tlr][]
* Replace "/Library/Input Methods/LipikaIME.app/Contents/Resources/Schemes/Script/Devanagari.map" with this updated [Devanagari.map][]
* Then kill LipikaIME from Activity Monitor and restart it

[LipikaIME]: https://github.com/ratreya/Lipika_IME/wiki
[ITRANS.tlr]: https://raw.githubusercontent.com/aupasana/Lipika_IME/master/Common/Resources/Schemes/Transliteration/ITRANS.tlr
[Devanagari.map]: https://raw.githubusercontent.com/aupasana/Lipika_IME/master/Common/Resources/Schemes/Script/Devanagari.map

### notes

* The two files above are protected (root access only), and they are in a hidden location (finder won't show them). Download the files, and then launch "terminal" and use the "sudo cp" command to replace the files.
* if there are any extended macOS permissions, the Lipika IME menu items may not show up correctly. Use "ls -@la" to see the extended permissions on the files you have copied, and remove them using "xattr -d [permission]". Log out and back in and the menu should now render correctly.
* [[ link ][yt]] A youtube HD screencast -- "typing devanagari on OSX using lipika"

[yt]: https://www.youtube.com/watch?v=E1GHlcYE8NQ

## DLI Downloader

### windows

[[ link ][dli]] mudgala dli downloader (version 1.00)

The digital library of india (link) has a vast repository of sanskrit texts. Unfortunately, it's user interface makes it very difficult to search and download texts for offline use. This is a small tool for microsoft windows that allows a user to quickly search, download, and convert downloaded pages to pdfs for offline use.

[dli]: https://sites.google.com/a/aupasana.com/public/software/dli

### mac OSX

[[ link ]](https://raw.githubusercontent.com/aupasana/aupasana/master/OSXScripts/dli.py){:target="_blank"}
	dli.py -- a python script to deal with the entire workflow around downloading files from the digital library of India.

* search known DLI servers for books by barcode
* check DLI servers with the barcode to see if they have the files
* download the file from the server with multiple processes
* convert the files into a single PDF file
* resize the PDF file so all pages have a consistent page size

Please ensure the following tools are installed and available in the default path: wget, tiffcp tiff2pdf and gs. These tools are a part of the "wget", "libtiff / libtiff-tools" and "ghostscript" packages and can be downloaded using homebrew, apt-get etc. Then, install the python lxml module with "pip install lxml"

The simplest way to use the script is to specify the barcode alone. It will find a server that has the files and will create a file named "title_barcode.pdf" if the python lxml module is installed, and "barcode.pdf" otherwise.

~~~
> dli.py BARCODE
> dli.py --help
~~~

### dependencies

~~~
brew install wget libtiff ghostscript         (on mac osx)
apt-get install libtiff-tools python aria2    (on debian)
choco install python2 gow ghostscript aria2   (on windows)
~~~


### notes (windows only)

You must now install libtiff manually, since it isn't supported by chocolatey

* download both the "binaries" and "dependencies" zip files from
	<br>http://gnuwin32.sourceforge.net/packages/tiff.htm
* extract the contents of the "bin" folder from both zip files into a single folder
* add the path to the folder which contains these binaries to your PATH

XArgs parallelism doesn't work on windows. Use the aria tool, since it supports parallelism natively.

~~~
> dli.py BARCODE --download-tool aria
~~~
