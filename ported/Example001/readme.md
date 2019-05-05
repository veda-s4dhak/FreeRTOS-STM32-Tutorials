Example 1. Creating tasks
This example demonstrates the steps needed to create two simple tasks, then start the tasks executing. The tasks simply print out a string periodically, using a crude null loop to create the period delay. Both tasks are created at the same priority, and are identical except for the string they print out. 

Note in the STM32 implementation rather than printing 2 counters (task_heartbeat) are implemented.
