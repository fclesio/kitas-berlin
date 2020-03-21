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

Running Die kleine Ziege in your machine
------------------------------
1) Enter in the Kita Navigator website: https://www.kita-navigator.berlin.de/ and click in the Kitas Finden. This will open the search (suche) option

2) In the suche (search) screen (https://www.kita-navigator.berlin.de/suche) put your address and the radius. After that click in the blue button with will contains the number of kitas available fdor your search 

3) After that a screen with all the kitas will open. Copy the URL.
https://www.kita-navigator.berlin.de/einrichtungen?input=Arnold-Knoblauch-Ring%2C%2014109%20Berlin%2C%20Alemanha&betb=2-2020&einfacheSuche=true&entfernung=5&lat=52.4099966&lon=13.137335

4) Run the following command:

    $ python3 ziege.py
    
5) The output will be two files (an excel file and a csv):
    `ziege.xlsx`
    `ziege.csv`

Why "Die kleine Ziege"?
------------------------------
Apparently, if you have a baby in Berlin everything it's rigged to make your life harder; and find a Kita it's one of those endeavors that the local government uses to test your patience, resilience, and peace of mind.  Then, my life partner and I decided to write this wrapper. [__Die kleine Ziege__](https://www.dict.cc/?s=ziege) means "_little goat_" in German and this is the nickname of our first born. 
