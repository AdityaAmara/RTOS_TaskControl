# RTOS_TaskControl Program
This is a program for creating two different tasks (1. Serial Printing and 2. Temperature and Humidity reading with DHT11) and control the tasks using different functions in FreeRTOS library.

# Requirements: 
1. Arduino IDE
2. FreeRTOS Library included in Arduino IDE
3. Arduino Board (Arduino UNO, Nano, Mega..etc)

# Functions we use:
1. **vTaskDelay ()**  - vTaskDelay() specifies a time at which the task wishes to unblock relative to the time at which vTaskDelay() is called. For example, specifying a block period of 100 ticks will cause the task to unblock 100 ticks after vTaskDelay() is called. vTaskDelay() does not therefore provide a good method of controlling the frequency of a periodic task as the path taken through the code, as well as other task and interrupt activity, will effect the frequency at which vTaskDelay() gets called and therefore the time at which the task next executes. See vTaskDelayUntil() for an alternative API function designed to facilitate fixed frequency execution. It does this by specifying an absolute time (rather than a relative time) at which the calling task should unblock.
2. **uxTaskPriorityGet ()** - vTaskDelay() obtains the priority of the task.
3. **vTaskPrioritySet ()** - vTaskPrioritySet () sets the priority of any task. A context switch will occur before the function returns if the priority being set is higher than the currently executing task.
4. **vTaskSuspend ()** - vTaskSuspend () suspends any task. When suspended a task will never get any microcontroller processing time, no matter what its priority. Calls to vTaskSuspend are not accumulative – i.e. calling vTaskSuspend () twice on the same task still only requires one call to vTaskResume () to ready the suspended task.
5. **vTaskResume ()** - vTaskResume () resumes a suspended task. A task that has been suspended by one or more calls to vTaskSuspend () will be made available for running again by a single call to vTaskResume ().

# Procedure:
1. Connect the circuit as below
