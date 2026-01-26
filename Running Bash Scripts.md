#programming #programming/bash 

# Running Bash Scripts

The **file extension** for a **shell script** is: *.sh*
However, **linux** by default does **not** allow programs to be run. We need to allow this by using the **chmod** command:

```bash
chmod +x script.sh # Allows the script to be run
chmod u+x script.sh # Allows the script to be run only by the user
```