# Lab Report 3

## The Interesting Commands of grep

I decided to choose my commands from the command of grep which allows you to search for a specific string in 
either a file, filename, or even extension. 


### grep whatwordwewant logfile.txt | grep -v whatwordweavoid

[How to ignore some words while doing a search using grep](https://javarevisited.blogspot.com/2011/06/10-examples-of-grep-command-in-unix-and.html#axzz81MdcXFPV)\
**Example 1 of Ignoring Words:**
```
grep now technical/911report/chapter-1.txt | grep -v the
    Terminal: Got him just out of 9,500-9,000 now.
    Center: Do you know who he is?
    Terminal: We're just, we just we don't know who he is. We're just picking him up now.
    FAA Headquarters: Oh, God, I don't know.
```
**Example 2**

```
grep to technical/plos/journal.pbio.0020001.txt | grep -v the
    invested in research and development for each region, also show that, in contrast to both
    of publications per amount of money allocated to research and development in Latin America,
    concluded that, as a group, Latin America could afford to invest a much higher proportion
    United States could reflect a trend towards more costly research in larger scientific
    Science ; with impact factors of 27.96 and 23.33, respectively and in
    papers to become a highly cited scientist. It requires attending international meetings and
    A Long Road Yet to Travel
```

This command is taking a search for a specfic word in my cases "now" and "to" and is then searching for all the cases these words occur where in that same line there are no occurances of the second grep command, which in this case is "the". There is immediate usefulness to using the grep command this way. It demonstrates a way of pruning the output of very long searches while searching for the specific word you want to know. 

### grep -v -e "pattern" -e "pattern" filename.txt

[Display the lines which does not matches all the given pattern](https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/)\
**Example 1 of : Displaying lines which don't match**

```
grep -v -e "the" -e "law" -e "which" technical/government/Media/5_legal_Groups.txt

Vulnerable
Salt Lake City Tribune

BY EDWARD MCDONOUGH
Five independent Salt Lake organizations that provide legal
Legal Center at 205 N. 400 West is a project of "And Justice for
agencies about $375,000 each year. My assistant, Charity
efficient for those needing legal services. No longer will a woman
desperate for a protective order, for example, have to run all over
brick and stone interior walls were all hidden behind coverings and
Sweet Candy Company building for Tomax. The Olafsons are delighted
cost received so far. There still needed to be furnishings and
```

**Example 2**


```
grep -v -e "the"  -e "and" -e "for" technical/government/Media/5_legal_Groups.txt

Vulnerable
Salt Lake City Tribune

BY EDWARD MCDONOUGH
Five independent Salt Lake organizations that provide legal
All," which, until this venture, has been a joint fund-raising
service law groups.
agencies about $375,000 each year. My assistant, Charity
```

This command acts as a black list, where it will block lines that contain what appears in the pattern decided upon and everything else is let through to the terminal. This is useful moreso for some of the smaller files or for finding out which words appear to be having the largest impact on a file based on how much the size of the file changes based on what gets blacklisted. 

### grep “^placeholderword” file1
[Match all lines that start with ‘placerholderword’](https://www.softwaretestinghelp.com/grep-command-in-unix/)\

**Example 1 of Finding lines that start with a word:**

```
grep "^the" technical/911report/chapter-1.txt
    the hijacked aircraft would be readily identifiable and would not attempt to disappear;
    there would be time to address the problem through the appropriate FAA and NORAD chains of command; and
    the hijacking would take the traditional form: that is, it would not be a suicide hijacking designed to convert the aircraft into a guided missile.
```

**Example 2**


```
grep "^FAA" technical/911report/chapter-1.txt
    FAA Awareness. Although the Boston Center air traffic controller realized at an early stage that there was something wrong with American 11, he did not immediately interpret the plane's failure to respond as a sign that it had been hijacked. At 8:14, when the flight failed to heed his instruction to climb to 35,000 feet, the controller repeatedly tried to raise the flight. He reached out to the pilot on the emergency frequency. Though there was no response, he kept trying to contact the aircraft.
    FAA Awareness. One of the last transmissions from United Airlines Flight 175 is, in retrospect, chilling. By 8:40, controllers at the FAA's New York Center were seeking information on American 11. At approximately 8:42, shortly after entering New York Center's airspace, the pilot of United 175 broke in with the following transmission:
```

This command will basically do a search of all the lines that begin with the specfic string. The interesting thing is that it does not start at the first occurance of a word in a line but with the actual first string meaning that if the word is indented that it has struggles finding the first occurance of that word. However we can accomadate for this and this tool is still useful in helping find lines that would begin with the word you are looking for. 


### ls ~/path/ or  ls /directory/ | grep ".file extension"

[Find Filenames Using Extensions](https://www.makeuseof.com/grep-command-practical-examples/?newsletter_popup=1)\

**Example 1 of Finding files that use certain Extensions:**

```
ls | grep ".md"
    index.md
    Lab Report 1 - Remote Access and FileSystem.md
    Lab Report 2 - Servers and Bugs.md
    Lab Report 3.md
    lab1-file.md
```

**Example 2**


```
ls technical/government/Alcohol_Problems | grep ".txt"
    DraftRecom-PDF.txt
    Session2-PDF.txt
    Session3-PDF.txt
    Session4-PDF.txt
```

This command works by utilzing the output of the ls command, which will display all the files in the current working directory by performing a search on the files. It can specfically target the file extensions which can further shrink the search of a type of file in your working directory to make sure that it is visible. It can also help clarify what type of files some are and specficify what you are looking for and overall is a powerful tool.