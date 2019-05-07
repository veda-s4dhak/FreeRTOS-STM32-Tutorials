Example 3. Experimenting with priorities

The scheduler will always ensure that the highest priority task that is able to run is the task
selected to enter the Running state. In our examples so far, two tasks have been created at
the same priority, so both entered and exited the Running state in turn. This example looks at
what happens when the priority of one of the two tasks created in Example 1 is changed. This
time, the first task will be created at priority 1, and the second at priority 2.

The scheduler will always select the highest priority task that is able to run. Task 2 has a
higher priority than Task 1 and is always able to run; therefore, Task 2 is the only task to ever
enter the Running state. As Task 1 never enters the Running state, it never prints out its
string. Task 1 is said to be ‘starved’ of processing time by Task 2. 
