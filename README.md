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

So my primary modification has been to extract the sounds from the .swf file,
and use conventional javascript functions to select and play those sounds.
That *should* make the program work with sound on all browsers.

A second bug fix was that if 'Grow balls on bounce' was turned off, the bouncing balls
didn't function correctly.  I fixed that as well.

Another mod that I _may_ make, is to try to make color selection for the lines be more consistent;
they seem to be somewhat random at this point.  This will take significantly more
effort, though, as the mechanism for selecting and propagating colors for the balls
is far from evident in the code.

##  historical notes
> Thaoh had included the following note on the 'Help' display, in his version of this program.
I do not actually have any idea what his note about 'Tracing' refers to, and I have seen *no*
impact from trying any value for the tracing field.  So I'm removing that comment and replacing 
it with info about me... but I will retain the note here, in case it has meaning for someone
in the future:

'Tracing' needs about 50 for you to see an effect at all, 
a higher tracing number will speed up the running of the script.


##  Bugs

There is one major bug present in this application... if user gets many balls in play
(15 or so seems to be sufficient), with sounds turned on, the sounds will get confused
and the program will completely lose control of them.  

One result of this bug, is that the sounds become irregular, and it does not appear that 
all sounds are actually present (there should be one sound for each ball, though the 
actual sounds wrap at 39 balls).  The second result of this bug, is that if you turn 
sounds off, they don't actually stop!!  

Later note: this bug actually only occurs with Firefox browser, 2021 version.
It does *not* occur with Chrome, at least with 20 balls in flight.

I have *no* firm idea what is causing this bug, so it is unlikely that I'll be able to fix it...

1. My initial guess was that the javascript Audio:play() function runs to completion before
another call can begin, and after awhile it just runs out of time to get all the sounds
generated before the next cycle begins.

2. Another possibility is that I simply need to pre-allocate all 39 sound objects,
before beginning to generate sounds.  In the current code, I allocate a new Audio
object every time I want to generate a sound.  That is clearly inefficient, even though
Java has garbage collection.  However, it doesn't appear to me that the program is
actually generating an index for each sound, so the traditional technique of 
pre-allocating Audio objects for all 39 sound files, isn't trivially done.
Maybe someone else who knows java better than I do (my expertise is C, not java/html), 
could someday try to optimize this process??


##  Licensing for this program
Josh Nimoy's original github repository has a Creative Commons license, 
and my derivations of his program will also be released under that license.
His original LICENSE file is included in this repository.

