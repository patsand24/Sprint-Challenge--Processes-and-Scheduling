### 1. List all of the main states a process may be in at any point in time on a standard Unix system. Briefly explain what each of these states mean.

- Created, Ready, Running, Blocked, Terminated

    - Created: State where a process is waiting to be moved into ready state after is is first created.

    - Ready: Ready or Waiting to be processed(think of it as being in a queue in main memory and is waiting to be executed).

    - Running: The process is now being run by the cpu and after that process is chosen and is either ran in kernal mode or user mode.

    - Blocked: This happens when a process is stopped from executing due to needing an external event occuring first such as a user input.

    - Terminated: When a process is finished executing it is then terminated or if it is killed explicitly.

### 2. What is a Zombie Process? How does it get created? How does it get destroyed?

- The process that happens after the terminated state is hit but is still waiting for the parent to read the exit status when it can then be removed from the process table to finally get destroyed.

### 3. Describe the job of the Scheduler in the OS in general.

- It allocates system resources to different tasksp prioritizing processes that are in the ready state and determining the amount of time to be allocated to these processes.

### 4. Describe the benefits of the MLFQ over a plain Round-Robin scheduler.

- A Round-Robin Scheduler doesn't prioritize the cpu time for different processes, instead spreading them out all at once(round-robin) which can lead to performance problems. On the flip side, MLFQ is changing priority of the processes and will make decisions in real time based on the behavior of processes, such as certain ones taking to long(these will be moved dowon in priority) which imporves overall performance.