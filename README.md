# Tutorial 10 reflection

## Experiment 1.2: Understanding how it works.

![image](https://github.com/Sirered/adprog-tutorial10/assets/126568984/586fc484-8741-438c-b2f7-931881ffe4d9)

The reason as to why the hey hey occured before the howdy, is due to the fact that the lines that are placed in the spawner start being done asynchronously when you do executor.run(), which occurs after the printing of hey hey

## Experiment 1.3: Multiple Spawn and removing drop

### Multiple Spawn
![image](https://github.com/Sirered/adprog-tutorial10/assets/126568984/7fbea505-1edb-4288-8eab-d1ac33c8e07d)

The executor.run() use a while loop to iterate through all of the tasks that were spawned and initiate them, however it does not have to wait for one task to complete before initiating the next. Because of this, he initiates all 3 tasks asynchronously without any delay, thus printing all of the howdy's at once, then only after each of those threads have waited 2 seconds, do they all print out all the dones at once.

## Remove drop
![image](https://github.com/Sirered/adprog-tutorial10/assets/126568984/e45a2ec3-1c84-4156-8735-9e33daa4e539)

From here, we see that even after all of the tasks were run, the program isn't terminating. This is because there is still a thread holding the spawner that is keeping the spawner and thus the entire program alive. If we don't drop spawner and let it be, the thread and program will continue to run.
