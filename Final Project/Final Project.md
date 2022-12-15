---
Angelo Castillo
Class: Cis106
---

## Question 1

For every command in this list, include the following:

### Description
### formula/syntax
### 3 examples that you understand well

## awk
Description:
Awk is a scripting language used for manipulating data and generating reports.
 The name of the cat command comes from its functionality to concatenate files. It can read, concatenate, and write file contents to the standard output. 
 Formula:
 `awk options 'selection _criteria {action }' input-file > output-file` 
 Example:
 1. If you wish to list all the lines and columns in a file.
  `awk ' {print $0}' file.txt`
  2. To match all entries with the letter ‘c’
  `awk '/c/ {print $0}' file.txt`
  3. To print the first and second columns
   `awk '{print $1 "\t" $2}' file.txt`

## cat
Description:
 The name of the cat command comes from its functionality to concatenate files. It can read, concatenate, and write file contents to the standard output.
Formula:
`cat > file1.txt`
Examples:
Use the -s option to omit the repeated empty output lines:
`cat -s file.txt`
To display the invisible line ending character use the -e argument:
`cat -e /etc/lsb-release`
read the contents of file1.txt and file2.txt 
`cat file1.txt file2.txt`

## cp
Description:
cp is a command-line utility for copying files and directories on Unix and Linux systems.
Formula:
`cp [OPTIONS] SOURCE... DESTINATION`
Example
Copying Files with cp Command 
`cp file file_backup`
To copy a file to another directory, specify the absolute or the relative path to the destination directory.
`cp file.txt /backup`
Copy Multiple Files and Directories #
`cp file.txt dir file1.txt  dir1`

## cut
Description:
cut is a command-line utility that allows you to cut parts of lines from specified files or piped data and print the result to standard output.
Formula:
`cut OPTION... [FILE]...`
Examples:
to display the 1st and the 3rd field you would use
`cut test.txt -f 1,3`
 to display the 1st and 3rd fields using “:” as a delimiter, you would type:
`cut test.txt -d ':' -f 1,3`
print all field except the 1st and 3rd:
`cut test.txt -f 1,3 --complement`
## grep
Description:
grep searches one or more input files for lines that match a given pattern and writes each matching line to standard output.
Formula:
`grep [OPTIONS] PATTERN [FILE...]`
Examples:
to display all the lines containing the string bash from the /etc/passwd file, you would run the following command:
`grep bash /etc/passwd`
Use [ ] (brackets) to match any single character enclosed in the brackets.
`grep "acce[np]t" file.txt`
Use [^ ] to match any single character not enclosed in the brackets.
`grep "co[^l]a" file.txt`
## head
Description:
The head command prints the first lines (10 lines by default) of one or more files or piped data to standard output.
Formula:
`head [OPTION]... [FILE]...`
Examples:
Display a Specific Number of Lines 
`head -n <NUMBER> filename.txt`
For example, to display the first 100 bytes of data from a file
`head -c 100 filename.txt`
Display Multiple Files 
`head filename1.txt filename2.txt`

## ls
The ls command lists files and directories within the file system, and shows detailed information about them.
Formula:
`ls [OPTIONS + FILES]`
EX: 
to list the contents of the /etc directory, you would type:
`ls /etc`
pass multiple directories and files separated by space:
`ls /etc /var /etc/passwd`
To display all files including the hidden files use the -a option:
`ls -la ~/`

## man
Man command in Linux is used to display the user manual of any command that we can run on the terminal.
Formula:
`man [OPTION][COMMAND NAME}`
EX:
display only a specific section of a manual.
 `man [SECTION-NUM] [COMMAND NAME]`
  -f option, this option gives the section in which the given command is present.
   `man -f [COMMAND NAME]`
-w option: This option returns the location in which the manual page of a given command is present.
`man -w [COMMAND NAME]`


## mkdir
MKDIR allows you to create directories (also known as folders).
formula:
`mkdir [OPTION] [DIRECTORY]`
EX:
To create a directory in Linux
`mkdir newdir`
To create a new directory in another location
`mkdir /tmp/newdir`
How to Create Parent Directories 
`mkdir /home/linuxize/Music/Rock/Gothic`
## mv
The mv command is used to rename and move and files and directories from one location to another.
Formula:
mv [OPTIONS] SOURCE DESTINATION
Ex:
to move the file file1 from the current working directory to the /tmp directory you would run:
`mv file1 file2`
Moving Multiple Files and Directories 
`mv file1 file2 dir1`
The mv command also allows you to use pattern matching.
`mv *.pdf ~/Documents`
## tac
Tac command in Linux is used to concatenate and print files in reverse.
Formula:
`tac [OPTION][FILE]`
Ex:
 It will print files in reverse.
 `tac tacexamplecis106.txt`
 tac -s : This option use STRING as the separator instead of newline.
 `tac -s concat.txt tacexample.txt`

## tail
The tail command displays the last part (10 lines by default) of one or more files or piped data.
Formula:
`tail [OPTION][FILE]`
EX:
 display the last 10 lines.
 `tail filename.txt`
 How to Display a Specific Number of Lines.
`tail -n <NUMBER> filename.txt`
For example to display the last 500 bytes of data from the file named filename.txt you would use:
`tail -c 500 filename.txt`

## touch
The touch command allows us to update the timestamps on existing files and directories as well as creating new, empty files.
Formula:
For example, if the file file1 doesn’t exist the following command will create it otherwise, it will change its timestamps:
`touch file1`
To create or modify multiple files at once, specify the file names as arguments:
`touch file1 file2 file3`
If you don’t want the touch command to create new files, use the -c (--no-create) option.
`touch -c file1`

## tree
 tree is a recursive directory listing program that produces a depth-indented listing of files. 
 Formula:
 `tree + option + Files`
 EX:
 List files with their permissions.
 `tree -p ./GFG `
 Create files using tree command
`tree [-adfgilnopqrstuxACDFNS] [-L level [-R]] [-H baseHREF] [-T title] [-o filename]` 

## vim/nano
nano is an easy to use command line text editor for Unix and Linux operating systems.
Vim is another editor but more complex and challenging than nano.

Question 2
## Answer each question:
## How to work with multiple terminals open?
CTRL + Shift + N will open a new terminal window if you are already working in the terminal, alternatively you can just select "Open Terminal" from the file menu as well.

## How to work with manual pages?
To use man, you type man on the command line, followed by a space and a Linux command. man opens the Linux manual to the “man page” that describes that command if it can find it, of course.
## How to parse (search) for specific words in the manual page
Firstly you got a list of man pages corresponding to "bash" in their description, thereafter you iterate through the retrieved list and searching for matching brace expansion.
## How to redirect output (> and |)
The > symbol is used to redirect output by taking the output from the command on the left and passing as input to the file on the right.
## How to append the output of a command to a file
To redirect the output of a command to a file, type the command, specify the > or the >> operator, and then provide the path to a file you want to the output redirected to.
## How to use wildcards
To locate a specific item when you can't remember exactly how it is spelled, try using a wildcard character in a query.
 For copying and moving multiple files at the same time. EX `cp -r dir1/*.gif dir2`.
## How to use brace expansion
For creating entire directory structures in a single . It creates a folder structure like this work parent folder then F1,F2,F3 child folders and temp1 and temp2 child folders under three parent folder F1,F2,F3.
EX `mkdir -p work/{F1,F2,F3}/{temp1,temp2}`
