Die kleine Ziege: Find a Kita in Berlin
=====================================
Your virtual Jugendämt

*Die kleine Ziege* is a wrapper that fetch all Kita listings from [Kita Navigator Berlin](https://www.kita-navigator.berlin.de/suche) in Python.
 
Requirements
------------------------------

    $ pip3 install numpy
    $ pip3 install pandas
    $ pip3 install requests
    $ pip3 install beautifulsoup4
    $ pip3 install selenium
    $ pip3 install urllib3
    $ brew install geckodriver    

Warning
------------------------------
According to your search parameters and location, maybe more than 500 results will appear and it will take a while to fetch all. In my case took more than 2 hours to fetch 672 results.

This happens because the Kitas pages aren't simple HTML vanilla pages, but there's tons of JavaScript code contained, and it means that to scrap the information the page needs to be loaded with all elements and scrolled down.

I'll put some [`multiprocessing`](https://docs.python.org/3/library/multiprocessing.html) in some moment in the future to speed it up, but for now, enjoy your baby time and wait. Recommended music during the wait: _[Helge Schneider - Marihuana ist nicht gut](https://www.youtube.com/watch?v=nIVYqnL9cvM)_


Running Die kleine Ziege in your machine
------------------------------
0) Download the entire repo in your machine and start a `jupyter notebook` instance inside of this folder;

1) Enter in the [Kita Navigator website](https://www.kita-navigator.berlin.de/) and click in the Kitas Finden. This will open the search (suche) option;

2) In the [suche (search) screen](https://www.kita-navigator.berlin.de/suche) put your address and the radius. After that click in the blue button with will contains the number of kitas available fdor your search;

3) After that a screen with all the kitas will open. [Copy the URL](https://www.kita-navigator.berlin.de/einrichtungen?input=Arnold-Knoblauch-Ring%2C%2014109%20Berlin%2C%20Alemanha&betb=2-2020&einfacheSuche=true&entfernung=5&lat=52.4099966&lon=13.137335) and paste in the `base_search_urlpage` variable in the first notebook called [01-kita-url-extractor.ipynb](https://github.com/fclesio/kitas-berlin/blob/master/01-kita-url-extractor.ipynb);

4) Check the number of pages of your search and put this number in the `number_of_pagination` variable;

5) Run the [01-kita-url-extractor](https://github.com/fclesio/kitas-berlin/blob/master/01-kita-url-extractor.ipynb) notebook;

6) After that run the [02-kita-page-scrapper](https://github.com/fclesio/kitas-berlin/blob/master/02-kita-page-scrapper.ipynb) notebook; and 

7) The output will be a Pandas Dataframe.

Why "Die kleine Ziege"?
------------------------------
Apparently, if you have a baby in Berlin everything it's rigged to make your life harder; and find a Kita it's one of those endeavors that the local government uses to test your patience, resilience, and peace of mind.  Then, my life partner and I decided to write this wrapper. [__Die kleine Ziege__](https://www.dict.cc/?s=ziege) means "_little goat_" in German and this is the nickname of our first born. 
