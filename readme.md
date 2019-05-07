Example 1 -> Creating Tasks (initializing 2 basic tasks)
Example 2 -> Using the Task Parameter (making multiple tasks with the same task function)
Example 3 -> Experimenting with priorities (making one task have a higher priority than another)
Example 4 -> Using a blocked state to create a delay (A delay, using vTaskDelay, allows a task to enter the blocked state allowing other lower priority tasks to execute)
Example 5 -> Converting the example tasks to use vTaskDelayUtil (Using vTaskDelayUtil instead of vTaskDelay guarantees the task will run at a particular frequency)
Example 6 -> Combining blocking and non-blocking tasks (Running 2 tasks which do not have delays but are a lower priority than another task which has a delay but is at a highe priority)
Example 7 -> Defining an idle hook function (Running a process in the idleTask when higher priority tasks are in a blocked state)
Example 8 -> Changing Task Priorities (Changing the priorities of tasks dynamically during execution)
Example 9 -> Deleting Tasks (Demonstrating deletion of a task during execution)

Note: Next chapter is on types of scheduling algorithms available on FreeRTOS
  a) Prioritized Pre-emptive Scheduling (without Time Slicing)
  b) Cooperative Scheduling
  
