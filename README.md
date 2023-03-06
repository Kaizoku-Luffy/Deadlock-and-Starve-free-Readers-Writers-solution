# Deadlock-and-Starve-free-Readers-Writers-solution

In the pseudocode we use three semaphores:\
1.general_mutex (To make reader processes which entered the queue after writer processe wait).\
2.readers_mutex (Mututal exclusion for readers count).\
3.write_mutex (To make writer wait while reading).

All these semaphores are intialized to 1 at the start.

There is an integer variable(readers_count) intialized to 0 at the start.

In the code if reader process arrives first,then writer process must wait due to write_mutex semaphore.\
Multiple reader processes may enter critical section as general_mutex semaphore is set after readers counting.\
Reader process can't enter critical section as general_mutex semaphore is 0 while writer process in critical section.\
Multiple writer process cannot enter critical section.\

The code is starve free as the processes occur in the FIFO order so that it is fair to both processes.
