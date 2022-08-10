# CSCI_3500_A4

# Objective
The goal of this program is to explore the utility of a mutex when
developing multithreaded programs. The program creates a specified
number of threads that wait in the thread_code() function. The
threads wait for the first thread in main() to change the shared
variable, shared_variable, to 1. When a thread detects that
shared_variable has changed to 0, it attempt to change
shared_variable back to 0. All threads attempt this simultaneously
leading to descrepencies between the number of times
shared_variable is to 0 by the threads and the number of times
it is set to 1 by main. This competition is iterated based on the
iteration argument given at run-time. The inclusion of a mutex lock
prevents more than one thread to change the variable at a time. 

# Notes:
The program checks for the presents of a -sync argument. If
present, the mutex functionality is enabled. The next two arguments
become the number of threads and iterations respectively. 
