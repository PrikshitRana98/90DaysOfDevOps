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


**Task 01**

<img width="678" height="788" alt="Screenshot 2026-03-04 at 10 26 54 PM" src="https://github.com/user-attachments/assets/6a345ba2-a786-4546-9df9-692ff940e9ed" />
<img width="515" height="93" alt="Screenshot 2026-03-04 at 10 29 16 PM" src="https://github.com/user-attachments/assets/7576964d-1502-482a-9e71-ff9d4ada509d" />
