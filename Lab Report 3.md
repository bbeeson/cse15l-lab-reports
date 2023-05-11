# Lab Report 3

## The Interesting Commands of grep
Choose one of them. Online, find 4 interesting command-line options or alternate ways to use 
the command you chose. For example, we saw the -name option for find in class. For each of 
those options, give 2 examples of using it on files and directories from ./technical. Show 
each example as a code block that shows the command and its output, and write a sentence or 
two about what it’s doing and why it’s useful.

### grep Exception logfile.txt | grep -v ERROR

How to ignore some words while doing a search using grep
https://javarevisited.blogspot.com/2011/06/10-examples-of-grep-command-in-unix-and.html#axzz81MdcXFPV 


### grep -v -e "pattern" -e "pattern"
display the lines which does not matches all the given pattern


https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/

### grep “done$” file1
Match all lines that end with ‘done’. E.g: “well done”

https://www.softwaretestinghelp.com/grep-command-in-unix/

### ls ~/path/ or  ls /directory/ | grep ".file extension"

Find Filenames Using Extensions

https://www.makeuseof.com/grep-command-practical-examples/?newsletter_popup=1