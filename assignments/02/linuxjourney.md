# Linux Journey 
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
<br>
<br>
## 5. touch
### Exercise: 
1.Create a new file<br>
touch myfile
<br>
<br>
2.Note the timestamp<br>
-rw-r--r-- 1 tareh 197609 0 Nov  6 15:49 myfile
<br>
<br>
3.Touch the file and check the timestamp once again<br>
-rw-r--r-- 1 tareh 197609 0 Nov  6 15:55 myfile
### Quiz:
How do you create a file called myfile?<br>
Answer:  **touch** myfile
<br>
<br>
## 6. file
### Exercise:
Run the file command on a few different directories and files and note the output.<br>
**$ file /c/Users/tareh/Downloads/Cambridge.pdf**
<br> 
---> output: /c/Users/tareh/Downloads/Cambridge.pdf: PDF document, version 1.3, 1 page(s)
### Quiz:
What command can you use to find the file type of a file?<br>
Answer:  **file**
<br>
<br>
## 7.cat
### Exercise:
Run cat on different files and directories. Then try to cat multiple files.<br>
**$ cat myfile dogfile**
--> output: *The content of both files*
<br>
### Quiz:
What's a good way to see the contents of a file?<br>
Answer:  **cat**
<br>
<br>
## 8.less
$ less /home/pete/Documents/text1<br>
<br>Use the following command to navigate through less:<br>
<br>
q - Used to quit out of less and go back to your shell.<br>
Page up, Page down, Up and Down - Navigate using the arrow keys and page keys.<br>
g - Moves to beginning of the text file.<br>
G - Moves to the end of the text file.<br>
/search - You can search for specific text inside the text document. Prefacing the words you want to search with /<br>
h - If you need a little help about how to use less while you’re in less, use help.
### Exercise:
- [x] Run less on a file, then page up and around the file. Try searching for a specific word. Quickly navigate to the beginning or the end of the file.
### Quiz:
How do you quit out of a less command?
<br>Answer: **q**
<br>
<br>
## 9. history:
### Exercise:
- [x] Navigate through your previous command history with the Up and Down keys. Play around with ctrl-R reverse search.
### Quiz:
What is the command to clear the terminal?<br>
Answer: **clear**<br><br>
Use !!. If you typed cat file1 and want to run it again <br>
Hit ctrl-R and you start typing parts of the command you want 
## 10. cp (Copy)
### Exercise:
- [x] Copy over a couple of files, be careful not to overwrite anything important.
### Quiz:
What flag do you need to specify to copy over a directory?<br>
Answer: **cp -r**<br>
<br>
$ cp mycoolfile /home/pete/Documents/cooldocs
<br>mycoolfile is the file you want to copy and /home/pete/Documents/cooldocs is where you are copying the file to. <br>
<br>
-* the wildcard of wildcards, it's used to represent all single characters or any string.<br>
-? used to represent one character<br>
-[] used to represent any character within the brackets <br>
<br>
$ cp *.jpg /home/pete/Pictures <br>
This will copy all files with the .jpg extension in your current directory to the Pictures directory.<br>
<br>
-$ cp -r Pumpkin/ /home/pete/Documents
<br>r flag will recursively copy the files and directories within a directory<br>
<br>
-$ cp -i mycoolfile /home/pete/Pictures<br>
 use the -i flag (interactive) to prompt you before overwriting a file
<br>
<br>
## 11. mv (Move)
### Exercise: 
Rename a file, then move that file to a different directory.<br>
$ mv c/Users/tareh/OneDrive/Bilder/Screenshots/Screenshot(1).png Portfolio1.png<br>
$ mv c/Users/tareh/OneDrive/Bilder/Screenshots/Portfolio1.png /home/pete/Documents
### Quiz:
How do you rename a file called cat to dog? <br>
Answer: **mv cat dog**
<br>
<br>
You can rename files like this:<br>
$ mv oldfile newfile
<br>
<br>
Or you can actually move a file to a different directory:<br>
$ mv file2 /home/pete/Documents
<br>
<br>
And move more than one file:<br>
$ mv file_1 file_2 /somedirectory
<br>
<br>
You can rename directories as well:<br>
$ mv directory1 directory2
<br>
<br>
you can use the -i flag to prompt you before overwriting anything:<br>
mv -i directory1 directory2
<br>
<br>
Let’s say you did want to mv a file to overwrite the previous one. You can also make a backup of that file and it will just rename the old version with a ~:<br>
$ mv -b directory1 directory2
<br>
<br>
## 12. mkdir (Make Directory)
### Exercise: 
Make a couple of directories and move some files into that directory.
$ mkdir books paintings
### Quiz:
What command is use to make a directory?<br>
Answer:**mkdir**
<br>
<br>
You can also create subdirectories at the same time with the -p (parent flag).<br>
$ mkdir -p books/hemmingway/favorites
<br>
<br>
## 13. rm (Remove)
### Exercise:
1.Create a file called -file (don't forget the dash!).<br>
**$ touch -- -file**<br>
<br>
2.Remove that file.<br>
**$ rm -- -file**

### Quiz:
How do you remove a file called myfile?<br>
Answer: **rm myfile**
<br>
<br>
You can remove a directory with the rmdir command:<br>
$ rmdir directory
<br>
<br>
## 14. find
### Exercise:
Find a file from the root directory that has the word net in it.<br>
**$ find anaconda3/ -type d -name "*net*"**<br>
output---> *long list of files*

### Quiz:
What option should I specify for find if I want to search by name?<br>
Answer: **-name**
<br>
<br>
## 15. help
### Exercise:
Run help on the echo command, logout command and pwd command.<br>
**$ help echo**<br>
**$ help logout**<br>
**$ help pwd**
### Quiz:
How do you get quick command line help for built-in bash commands?<br>
Answer: **help**
<br>
<br>
## 16. man
### Exercise:
Run the man command on the ls command.
**$ man ls**
### Quiz:
How do you see the manuals for a command?<br>
Answer:**man**
<br>
<br>
## 17. whatis
### Exercise:
Run the whatis command on the less command.
### Quiz:
What command can you use to see a small description of a command?<br>
Answer: 
<br>
<br>
## 18.
### Exercise:
### Quiz:
<br>
<br>
## 19.
### Exercise:
### Quiz:
