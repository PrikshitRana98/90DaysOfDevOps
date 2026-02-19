Today’s goal is to build your Linux command confidence.

Process management
File system
Networking troubleshooting

** Process Management **
it is a running instance of any program like running a python script on linux server, or shell script on linux server

**Why Process Management is Important?**

Because a server is nothing but:

CPU + Memory + Running Processes

If a server is slow or crashing, usually:
One process is consuming high CPU
One process is using too much memory
A process is stuck (zombie)
A service failed to restart

⚙️ What Linux Does Internally

1️⃣ Process Creation

When you run a command:

Linux assigns a PID (Process ID)
It creates a parent-child relationship
Allocates memory
Schedules CPU time

2️⃣ Process Scheduling

Linux decides:
Which process runs first
How long it runs
Priority handling

This is handled by the kernel scheduler.


