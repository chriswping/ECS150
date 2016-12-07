Guang Xu 998309428
Emily Cheung 998326896
Chris Ng 998311403

We have two different boot images and sets of files for
these programs as our implementation made them incompatible 
with each other.


Program 1
Files modified for P1: tty.c tty.h termios.h

For this program we modified tty.c, tty.h and termios.h.
While logging in the user can hit control K which makes the os
go into a new state to await the entry of a number. Upon pressing
a number after control K, that many characters will be deleted 
and stored. The user is press to continue entering letters,
and press control Y at any time to re-enter the previously 
deleted characters. Afterwards the user can do this again, 
or backspace, etc.



Program 2
Files modified for P2: main.c alloc.c

For this program we modified main.c and alloc.c to make the os
allocate memory with the worst-fit implementation rather than
first-fit, which it currently uses. In alloc.c, we changed the alloc_mem 
function to change its memory allocation implementation. Unfortunately, 
we were not able to bind the display of holes in main memory to a function  
key and instead we had it print holes from alloc.c, which 
essentially spams the terminal and makes it unusable, but is
suitable for this program’s purposes.