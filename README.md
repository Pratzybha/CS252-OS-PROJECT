## 4.22 Writing a Multi-Threaded Program
Write a multithreaded program that calculates various statistical values for a list of numbers. This program will be passed a series of numbers on the command line and will then create three separateworker threads. One thread will determine the average of the numbers, the second will determine the maximum value, and the third will determine the minimum value.

For example, suppose your program is passed the integers 90 81 78 95 79 72 85

> The program will report \
> The average value is 82 \
> The minimum value is 72 \
> The maximum value is 95 

The variables representing the average, minimum, and maximum values will be stored globally. The worker threads will set these values, and the parent thread will output the values once the workers have exited. (We could obviously expand this program by creating additional threads that determine other statistical values, such as median and standard deviation.)

### Solution
First we define the global variables as asked in the question named average, maximum and minimum.

The other global variables used will be maximum size of an array, an array, count of an element, loop counter and an array nmed worker_threads of size three.

We define the input function in order to get values to be stored in an array.

We define 3 functions for start_routine - thread_average, thread_minimum, thread_maximum.

#### Screenshot of a test case:
![TEST CASE 4 221](/4-22-EVEN-OUTPUT.jpeg)
![TEST CASE 4 222](/4-22-ODD-OUTPUT.jpeg)

## 4.23 Writing a Multi-Threaded Program
Write a multithreaded program that outputs prime numbers. This program should work as follows: The user will run the program and will enter a number on the command line. The program will then create a separate thread that outputs all the prime numbers less than or equal to the number entered by the user.

### Solution
We define global array whose maximum size is alredy given. A variable N is also declared globally whose value will be the number below which we want all prime numbers to be displayed as an output of the program.

We define two functions named * printprime and * print . 
Printprime function checks for prime numbers from 2 to given number and makes the array value corresponding to that index 1. 
Print function prints the prime numbers from 2 to that number.

The threads are used to carry out aforementioned work.

#### Screenshot of a test case:
![TEST CASE 4 23](/4-23-OUTPUT.jpeg)

The C Program:

(https://gist.github.com/Jabiribn/e58bf13c678953891900e5f982b48037)  \ 
(https://stackoverflow.com/questions/26090901/find-prime-numbers-in-a-separate-thread) 

The PThread Data Types & Functions:

(https://man7.org/linux/man-pages/man3/pthread_create.3.html) \
(https://www.ibm.com/docs/en/zos/2.3.0?topic=functions-pthread-create-create-thread#ptcrea) \
(https://man7.org/linux/man-pages/man3/pthread_join.3.html) \
(https://www.ibm.com/docs/en/zos/2.3.0?topic=functions-pthread-join-wait-thread-end) \
(http://www.qnx.com/developers/docs/qnxcar2/index.jsp?topic=%2Fcom.qnx.doc.neutrino.getting_started%2Ftopic%2Fs1_procs_thread_attr.html)
