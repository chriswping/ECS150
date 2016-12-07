Guang Xu 998309428
Emily Cheung 998326896
Chris Ng 998311403

Files modified: proc.c, proc.h, dmp_kernel.c


Program 1


For this program we modified proc.c, proc.h and dmp_kernel.c.
In proc.h 
we declared an array in the process struct to store
the number of messages sent from a process.
In proc.c we increment the corresponding array element.
In dmp_kernel.c we print the matrix, binding it to the F7 key.
We overwrote the kmessages_dmp function as it served little purpose.
The output is a matrix showing the number of processes sent from
process i to process j.



Program 2

For this program we modified proc.c, the scheduler section, lines 539 to 551.
In the scheduler, we created a for loop checking each processes' CPU time
in the queue.  If the process at the head of the queue (new process) has a shorter CPU time, 
we give it more priority allowing it to catch up with the older process.
Also, we changed the code where "front" had equal to "time_left" to "front = 1".
This changes the scheduler from round robin into shortest time first.
