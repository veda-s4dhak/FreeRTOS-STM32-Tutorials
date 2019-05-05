Example 2. Using the task parameter

The two tasks created in Example 1 are almost identical, the only difference between them
being the text string they print out. This duplication can be removed by, instead, creating two
instances of a single task implementation. The task parameter can then be used to pass into
each task the string that it should print out. 

Note in the STM32 implementation rather than printing messages, a counter (task_heartbeat) has been implemented.
