Example 6. Combining blocking and non-blocking tasks

Previous examples have examined the behavior of both polling and blocking tasks in isolation.
This example re-enforces the stated expected system behavior by demonstrating an execution
sequence when the two schemes are combined, as follows.

1. Two tasks are created at priority 1. These do nothing other than continuously print out
a string. These tasks never make any API function calls that could cause them to enter the
Blocked state, so are always in either the Ready or the Running state. Tasks of this
nature are called ‘continuous processing’ tasks, as they always have work to do (albeit
rather trivial work, in this case). The source for the continuous processing tasks is
shown in Listing 26.

2. A third task is then created at priority 2, so above the priority of the other two tasks.
The third task also just prints out a string, but this time periodically, so uses the
vTaskDelayUntil() API function to place itself into the Blocked state between each print
iteration
