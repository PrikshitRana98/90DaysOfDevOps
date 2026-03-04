What is Shebang?

A shebang is the first line in a script file that tells the operating system which interpreter should execute the scrip

Here is a clean, copy-paste friendly version:

---

# What is Shebang?

A **shebang** is the first line in a script file that tells the operating system which interpreter should execute the script.

It always starts with:

```
#! 
```

Example:

```
#!/bin/bash
```

This tells the system:
"Run this script using Bash."

Other examples:

```
#!/usr/bin/env python3
#!/usr/bin/env node
#!/bin/sh
```

---

# How It Works

When you run a script like this:

```
./myscript.sh
```

The OS checks the first line.

If it sees:

```
#!/bin/bash
```

It runs the script using Bash.

If it sees:

```
#!/usr/bin/env python3
```

It runs using Python.

If it sees:

```
#!/usr/bin/env node
```

It runs using Node.js.

In short:

Shebang = Instruction for the OS about which program should execute the file.

---

# What Happens If You Don’t Write It?

It depends on how you run the script.

Case 1:

```
bash myscript.sh
```

This will work because you are manually telling the system to use Bash.

Case 2:

```
./myscript.sh
```

If there is no shebang:

* The system may throw an error
* Or it may use the default shell (which might not be Bash)
* The script may behave differently

Example:

If your script uses Bash-specific syntax like:

```
[[ condition ]]
```

But the system runs it with `sh`, it may fail.

---

# Why It Is Important

* Makes the script portable
* Ensures correct interpreter
* Avoids compatibility bugs
* Required for cron jobs
* Important in server/production environments

---

# Best Practice (Modern Way)

Instead of:

```
#!/bin/bash
```

Use:

```
#!/usr/bin/env bash
```

Reason:

`env` finds Bash dynamically from the system PATH.

This makes your script more portable across Linux, macOS, and servers.

---

How to take input in a Shell Script (Short Answer)

Use the read command.

Example:

#!/usr/bin/env bash

echo "Enter your name:"
read name

echo "Hello $name"

**One-line input**

read -p "Enter your age: " age
echo "Your age is $age"


**Task 01**

<img width="678" height="788" alt="Screenshot 2026-03-04 at 10 26 54 PM" src="https://github.com/user-attachments/assets/6a345ba2-a786-4546-9df9-<img width="577" height="349" alt="Screenshot 2026-03-04 at 11 43 02 PM" src="https://github.com/user-attachments/assets/989be25e-dc0a-4afb-af85-5ced20576117" />
692ff940e9ed" />
<img width="515" height="93" alt="Screenshot 2026-03-04 at 10 29 16 PM" src="https://github.com/user-attachments/assets/7576964d-1502-482a-9e71-ff9d4ada509d" />

**TASK 2**
<i<img width="516" height="83" alt="Screenshot 2026-03-04 at 11 05 31 PM" src="https://github.com/user-attachments/assets/d5762a11-bc63-45ee-821b-36dbee42b448" />
mg width="1073" height="638" alt="varibles1" src="https://github.com/user-attachments/assets/400f582a-cadb-4f74-8d09-867af30f6437" />

**Task3** 

<img width="834" height="546" alt="Screenshot 2026-03-04 at 11 40 33 PM" src="https://github.com/user-attachments/assets/8af8f64d-a57b-4d94-863f-c95f0d12d8d1" />
<img width="855" height="573" alt="Screenshot 2026-03-04 at 11 42 39 PM" src="https://github.com/user-attachments/assets/8cec5fe1-398f-48ef-80cf-952de827a5e7" />
<img width="577" height="349" alt="Screenshot 2026-03-04 at 11 43 02 PM" src="https://github.com/user-attachments/assets/d9c92dcb-9396-41ba-b049-d1027c2ad47c" />



