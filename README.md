## BallDroppings
An experimental javascript program which plays with bouncing balls on screen.

##  History of this program

This was originally released by Josh Nimoy in 2003.
At some point, though, the executable version of this program vanished from the web,
though the sources are still available at github:
https://github.com/jtnimoy/BallDroppings

Some time later, someone named Thaoh Myrdania distributed a modified version of this program,
with the main noticable change being that the lines and balls are in color.
http://www.thaoh.net/BallDroppings/#

Unfortunately, Thaoh *also* appears to have vanished from the internet; 
Most of the links on his page are dead, and the most recent activity by him appears to be back in 2016.

My modifications have been made on Thaoh's version, which I downloaded from his website.

##  My actions on this program
The one issue that I had with both previous versions of this program, is that they used
an swf (Flash) file to store the sounds.  On most browsers, the first call to the 'play sound' function
would hang the page.

So my primary modification will be to extract the sounds from the .swf file,
and use conventional javascript functions to select and play those sounds.
That *should* make the program work with sound on all browsers.

A second mod that I _may_ make, is to try to make color selection for the lines be more consistent;
they seem to be somewhat random at this point.

##  Licensing for this program
Josh Nimoy's original github repository has a Creative Commons license, 
and my derivations of his program will also be released under that license.
His original LICENSE file is included in this repository.
