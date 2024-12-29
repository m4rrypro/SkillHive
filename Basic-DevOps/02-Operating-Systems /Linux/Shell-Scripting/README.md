# Shell Scripting Basics
Shell scripting is a powerful tool for automating tasks in Linux. This section introduces the basics of writing and running shell scripts.

## What is Shell Scripting?
A shell script is a text file containing a series of commands that the shell can execute.

## Writing Your First Script
1. Open a terminal and create a file:
   touch first-script.sh

2. Add the following content to the file:
   #!/bin/bash
   echo "Welcome to SkillHive!"

   - `#!/bin/bash` specifies the script should be run using the Bash shell.
   - `echo` prints the message to the terminal.

3. Save the file and make it executable:
   chmod +x first-script.sh

4. Run the script:
   ./first-script.sh

## Practice Tasks
Try these beginner-friendly scripting exercises:
1. Write a script to display the current date and time.
2. Create a script that counts the number of files in a directory.
3. Automate creating a directory structure with subdirectories.
4. Write a script to check if a specific process is running and print its status.

## Tips for Learning
- Test your scripts frequently to ensure they work as expected.
- Use comments (#) to document your code and explain each step.
- Explore variables, loops, and conditionals for more advanced functionality.

## Resources for Learning
- Bash Scripting Basics: https://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO.html
- Shell Scripting Tutorial: https://www.shellscript.sh/
