Example 4. Using the Blocked state to create a delay

All the tasks created in the examples presented so far have been ‘periodic’—they have
delayed for a period and printed out their string, before delaying once more, and so on. The
delay has been generated very crudely using a null loop—the task effectively polled an
incrementing loop counter until it reached a fixed value. Example 3 clearly demonstrated the
disadvantage of this method. The higher priority task remained in the Running state while it
executed the null loop, ‘starving’ the lower priority task of any processing time.

There are several other disadvantages to any form of polling, not least of which is its
inefficiency. During polling, the task does not really have any work to do, but it still uses
maximum processing time, and so wastes processor cycles. Example 4 corrects this behavior
by replacing the polling null loop with a call to the vTaskDelay() API function, the prototype for
which is shown in Listing 22. The new task definition is shown in Listing 23. Note that the
vTaskDelay() API function is available only when INCLUDE_vTaskDelay is set to 1 in
FreeRTOSConfig.h.

vTaskDelay() places the calling task into the Blocked state for a fixed number of tick interrupts.
The task does not use any processing time while it is in the Blocked state, so the task only
uses processing time when there is actually work to be done.

Example 5. Converting the example tasks to use vTaskDelayUntil()

The two tasks created in Example 4 are periodic tasks, but using vTaskDelay() does not
guarantee that the frequency at which they run is fixed, as the time at which the tasks leave
the Blocked state is relative to when they call vTaskDelay(). Converting the tasks to use
vTaskDelayUntil() instead of vTaskDelay() solves this potential problem.
