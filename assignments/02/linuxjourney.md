## Linux Journey 
<br>

## 1.The Shell
### Exercise: 
Linux commands in Git Bash and what they output:
<br>
**$ date** 
<br> 
---> output: Tue Oct 29 12:00:30     2024 
<br>
**$ whoami** 
<br> 
---> output: tareh
### Quiz:
What should be outputted to the display when you type echo Hello World? 
<br>Answer: Hello World
<br>
<br>
## 2. pwd (Print Working Directory)
### Quiz:
How do I find what directory you are currently in? 
<br>Answer: **$ pwd**
<br>
<br>
## 3.cd (Change Directory)

$ cd .  (current directory). This is the directory you are currently in.
<br>$ cd .. (parent directory). Takes you to the directory above your current.
<br>$ cd ~ (home directory). This directory defaults to your “home directory”. Such as /home/pete.
<br>$ cd -  (previous directory). This will take you to the previous directory you were just at.

### Exercise: 
Run the cd command without any flags, where does it take you?
<br>Answer: When I type in  "cd ~"  it goes to the my home directory "/c/Users"
### Quiz:
If you are in /home/pete/Pictures and wanted to go to /home/pete, what’s a good shortcut to use?
<br>Answer: **cd ..**
<br>
<br>
## 4. ls (List Directories)
$ ls /home/pete: Lists the contents of the /home/pete directory.
<br>$ ls -a: Lists all files in the current directory, including hidden files (those starting with a dot).
<br>$ ls -la: Lists all files in the current directory in a detailed format, including hidden files, showing permissions, owner, group, size, and modification date.
### Exercise:
Run ls with different flags and see the output you receive.
<br> 
<br>ls -R: recursively list directory contents
<br>ls -r: reverse order while sorting
<br>ls -t: sort by modification time, newest first
### Quiz:
What command would you use to see hidden files?
<br>Answer: **ls -a**


