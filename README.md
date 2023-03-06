# Deadlock-and-Starve-free-Readers-Writers-solution

In the pseudocode we use three semaphores:\
1.general_mutex (To make readers processes which entered the queue after writer processe wait).\
2.readers_mutex (Mututal exclusion for readers count).\
3.write_mutex (To make writer wait while reading).

All these semaphores are intialized to 1 at the start.

There is an integer variable(readers_count) intialized to 0 at the start.
