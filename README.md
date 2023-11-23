# Sloppy Counter Simulator (sloppySim)

This C++ program simulates a sloppy counter, also known as an "approximate counter." The program uses multiple threads to perform work and updates a global counter with a specified level of sloppiness. The simulation can be configured with various command line arguments.

## Usage
Compile the program using the make command, which will create an executable named sloppySim. The program takes the following command line arguments:
./sloppySim <N_Threads> <Sloppiness> <Work_Time> <Work_Iterations> <CPU_Bound> <Do_Logging>

## Arguments
+ N_Threads: Number of threads to use. Defaults to 2 threads.
+ Sloppiness: Number of events before updating the global counter. Defaults to 10.
+ Work_Time: Average work time in milliseconds. Defaults to 10ms.
+ Work_Iterations: Number of iterations per thread. Defaults to 100.
+ CPU_Bound: "true" or "false" to indicate CPU-bound or IO-bound work. Defaults to "false."
+ Do_Logging: "true" or "false" to enable logging. Defaults to "false."

## Note
+ If the number of arguments is 3, all arguments after the third will be set to default.
+ If there is an error parsing the input, a message will be printed indicating the correct order of arguments.

## Code Description
The code creates a specified number of threads, and each thread performs work based on the provided parameters. The global counter is updated with the specified sloppiness. The program supports both CPU-bound and IO-bound work. Logging can be enabled to display settings and periodic updates of the global counter.

### Example
+ ./sloppySim 4 5 20 150 true true
+ This example runs the simulator with 4 threads, a sloppiness of 5, average work time of 20ms, 150 work iterations per thread, CPU-bound work, and logging enabled.

### Author
Jordan Wood (Copyright 2023)

### License
This program is provided under the copyright and license terms specified by Jordan Wood in 2023.
