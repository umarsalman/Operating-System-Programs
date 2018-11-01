# Operating-System-Scheduling-Programs in C++
Programs for operating system lab.
You can contribute to this repo by adding various operating system based algorithms in any language of your choice.
Make sure that your program contains required comments to make program more understandable for anyone using it.
All the contributers are requested to enter their information in the folder contributing.md (if not present, then make it and add your name).


A Process Scheduler schedules different processes to be assigned to the CPU based on particular scheduling algorithms. There are six popular process scheduling algorithms −

First-Come, First-Served FCFS Scheduling
Shortest-Job-Next SJN Scheduling
Priority Scheduling
Shortest Remaining Time (Preemptive version of SJN)
Round RobinRR Scheduling
Multiple-Level Queues Scheduling
Multiple-Level Feedback Scheduling
These algorithms are either non-preemptive or preemptive :

Non-preemptive algorithms are designed so that once a process enters the running state, it cannot be preempted(the control can’t be taken away from that process) until it completes its allotted time, wheres

preemptive scheduling is based on priority where a scheduler may preempt(the control can be taken away from that process) a low priority running process anytime when a high priority process enters into a ready state.

First Come First Serve

FCFS(Non Preemptive)

Jobs are executed on first come, first serve basis.
It is a scheduling algorithm.
Easy to understand and implement.
Its implementation is based on FIFO queue.
Poor in performance as average wait time is high.

Shortest Job Next

SJN

This is also known as shortest job first, or SJF
This can be preemptive or non-preemptive scheduling algorithm.
Best approach to minimize waiting time.
Easy to implement in Batch systems where required CPU time is known in advance.
Impossible to implement in interactive systems where required CPU time is not known.(As we can’t know which process will take less time)
The processer should know in advance how much time process will take.
Shortest Remaining Time

Shortest remaining time SRT is the preemptive version of the SJN algorithm.
The processor is allocated to the job closest to completion but it can be preempted by a newer ready job with shorter time to completion.
Impossible to implement in interactive systems where required CPU time is not known.
It is often used in batch environments where short jobs need to give preference.
SJN


Priority Based Scheduling

Priority scheduling may be preemptive or non-preemptive algorithm and one of the most common scheduling algorithms in batch systems.
Each process is assigned a priority. Process with highest priority is to be executed first and so on.
Processes with same priority are executed on first come first served basis.
Priority can be decided based on memory requirements, time requirements or any other resource requirement.

Round Robin Scheduling

Round Robin is the preemptive process scheduling algorithm.
Each process is provided a fix time to execute, it is called a quantum(Time Quantum).
Once a process is executed for a given time period, it is preempted and other process executes for a given time period.
Context switching is used to save states of preempted processes.

Multiple-Level Queues Scheduling

Multiple-level queues are not an independent scheduling algorithm. They make use of other existing algorithms to group and schedule jobs with common characteristics.

Multiple queues(Here queues are system process,interactive process etc.) are maintained for processes with common characteristics.
Each queue(Here queues are system process,interactive process etc.) can have its own scheduling algorithms.(As i can’t put them in one Queue and apply one Scheduling algorithm)
Priorities are assigned to each queue.
And the prioritiesv(higher to lower) are like :

System process(Highest priority)
Interactive Processs (ex:the CPU when wait for input from the keyboard, we have to keep its priority high,and this is a interactive process )
Batch Process
User Process(Lowest priority)
For example, CPU-bound jobs can be scheduled in one queue and all I/O-bound jobs in another queue. The Process Scheduler then alternately selects jobs from each queue and assigns them to the CPU based on the algorithm assigned to the queue.


Advantages is that we can apply separate Scheduling algorithms for separate processes/queue.

Disadvantage if any Higher Priority process/queue is there Lower Priority process/queue can’t get execute So,there may be a starvation situation for Low Priority Processes. This is the Disadvantage of this Scheduling algorithm.

Multiple-Level FeedBack Scheduling :

To eliminate the above Disadvantages what we do is, not let any process/queue to wait more than a specific time.if it wait more than that time just move that queue to upward by increasing it’s priority. ans we repeat this process until it get execute .so that there will be no more Starvation situation.

How can you change priority? and what Scheduling algorithm you gonna use to execute the top level queue(as it doesn’t support separate Scheduling algorithms for separate processes/queue.)?

it totally depends on the implementation.


