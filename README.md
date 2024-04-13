# A Kernel Seedling
In order to run this program you will need to compile a c file and then start a kernel with the compiled module. From there /proc/count will be modified and will contain the number of running processes. After running the kernel the compiled files and kernel need to be cleaned up by being removed. 

## Building
```shell
TODO: make
```
First the code must be compiled in order to build the kernel module. To do this run the Makefile with the command file which will compile and run the code to build the executables and kernel module. 

## Running
```shell
TODO: sudo insmod proc_count.ko
```
This code will load your compiled kernel module run it by running the module_init() function as it is insmoded into the kernl which will run the proc_count_init() function.

TODO: results?

At the end you should be able to check the results of the code by running the following command:
```shell
TODO: cat /proc/count
```
which should print out the number of processes running if the show function is correctly written in the proc_count.c file to count the number of running processes.

## Cleaning Up
```shell
TODO: make clean
/     sudo rmmod proc_count.ko
```
Run this after you are done running and using the code to get rid of executables and to clean up the kernel as this will run the module_exit() function which calls proc_count_exit() right before the program is rmmodded. 

## Testing
```python
python -m unittest
```
TODO: results?
The code should report OK if the function is run without a problem.

```shell
uname -r -s -v
```

The module was tested on Linux 5.14.8-arch1-1 #1 SMP PREEMPT Sun, 26 Sep 2021 19:36:15 +0000
