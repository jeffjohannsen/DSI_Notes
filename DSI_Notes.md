
# Command Line

[DSI Lecture "Just enough command line"](https://github.com/GalvanizeDataScience/lectures/blob/Denver/unix/chris-reger/Unix.pdf)  
[Unix/Command Line Tutorial](http://www.ee.surrey.ac.uk/Teaching/Unix/)  
[Command Line Quick Reference](https://github.com/GalvanizeDataScience/course-outline/blob/20-10-DS-DEN_DEN19/quick-reference/LinuxUnix.pdf)  
Codecademy Quick Explanations: [1](https://www.codecademy.com/articles/command-line-commands), [2](https://www.codecademy.com/learn/learn-the-command-line/modules/learn-the-command-line-navigation/cheatsheet)

## Helper Commands that make everything easier.
* `clear` - Clears the terminal.
* `exit` - Exits the terminal.
* `man` *`command_name`* - Opens the manual for the command.
* <kbd>Tab</kbd> to autocomplete the line.
* Up or down arrows to scroll through previous commands.
* <kbd>Ctrl + C</kbd> to kill a job

## Common Commands

|Command|Meaning|
|----------|:-------------|  
|**ls**|lists the contents of your current working directory|  
|**ls -a**|lists all files and directories including hidden ones|
|**ls -l**|long descriptions|
|**ls -S**|sort by size|
|**ls -T**|sort by time last modified|
|**mkdir** *name_of_directory*|make a new directory|
|**touch** *name_of_file*|make a new file|
|**pwd**|shows the current working directory|
|**cd** *name_of_directory*|change directory|  
|**cd .**|change to current directory|
|**cd ..**|change to parent directory (one level up the tree/file structure)|
|**cd** or **cd ~**|change to home directory|
|**mv** *file_name* &nbsp;*new_file_location*|move a file to a new directory|
|**mv** *file_name* &nbsp;*new_file_name*|rename a file|
|**cp** *original_file_name* &nbsp;*new_file_name*|make a copy of a file|
|**rm** *file_name*|removes(deletes) the file|
|**rm -f** *file_name*|force deletion of the file if it is protected|
|**rm -r** *file_name*|recursive delete. removes all subfolders and files within the directory|
|**Exploring Files**||
|**cat** *file_name*|displays the contents of the file|
|**less** *file_name*|displays the contents of the file one page at a time|
|**head** *file_name*|displays the first ten lines of the file|
|**tail** *file_name*|displays the last ten lines of the file|
|**wc -w** *file_name*|word count of file|
|**wc -l** *file_name*|line count of file|
|**sort** *file_name*|sorts each line of file alphabetically|
|**uniq** *file_name*|removes duplicate lines|

` `  
` `  
## Simple searching using less

[How to use the **less** command](https://linuxize.com/post/less-command-in-linux/)  

Using less, you can search though a text file for a keyword (pattern). For example, to search through science.txt for the word 'science', type

    $ less science.txt

then, still in less, type a forward slash [/] followed by the word to search

    /science

As you can see, less finds and highlights the keyword. Type [n] to search for the next occurrence of the word.

` `  
` `  
## Searching using grep “global regular expression print”

grep is one of many standard UNIX utilities. It searches files for specified words or patterns. First clear the screen, then type

    $ grep science science.txt

As you can see, grep has printed out each line containg the word science.

Or has it ????

Try typing

    $ grep Science science.txt

The grep command is case sensitive; it distinguishes between Science and science.

To ignore upper/lower case distinctions, use the -i option, i.e. type

    $ grep -i science science.txt

To search for a phrase or pattern, you must enclose it in single quotes (the apostrophe symbol). For example to search for spinning top, type

    $ grep -i 'spinning top' science.txt

Some of the other options of grep are:  
**-v** display those lines that do NOT match  
**-n** precede each matching line with the line number  
**-c** print only the total count of matched lines
**-R** recursive. search all files in a directory
**-c** count of occurances


## Pipes
![Pipes Explanation](images/command_line_pipes.png)

## Redirection
## **>**  

    $ cat oceans.txt > continents.txt
**>** takes the standard output of the command on the left and redirects it to the file on the right.

## **>>**
    $ cat glaciers.txt >> rivers.txt
**>>** takes the standard output of the command on the left and appends (adds) it to the file on the right.

## **<**
    $ cat < lakes.txt
**<** takes the standard input from the file on the right and inputs it into the program on the left.

## Advanced File and Directory Info
![File and Directory Info](images/command_line_directory_and_file_info.png)

## File and Directory Permissions
![File and Directory Permissions](images/command_line_file_and_directory_permissions.png)

## Running Python Files
* From the Command Line: `python name_of_file.py`
* Within IPython: `run name_of_file.py`
## Running Python Files with Inputs - Argparse
Can run python files and specify the inputs/arguments for the python file, all from the command line.  
[Argparse Tutorial](https://docs.python.org/3/howto/argparse.html)  

Examples:  

    $ python main.py --mode train --data training.csv --model price_predictor.pkl  
Python runs `main.py`, which uses command line argument parsing (Argparse) to take in arguments that affect how `main.py` executes. Here, `main.py` is running in train mode, so it will be expecting data with labels to train on in `training.csv`. After training, `main.py` will save the model and serialize it (pickle it), naming in `price_predictor.pkl`.

    $ python main.py --mode predict --data june.csv --model price_predictor.pkl --out predictions.csv  
Now `main.py` is running in predict mode, so it isn’t expecting labels with the `june.csv` data. `main.py` is using the earlier trained model (`price_predictor.pkl`)to make the predictions, and saving those predictions in `predictions.csv`.

# Git and GitHub

# Python Basics

# Python OOP

# Linear Algebra

# Numpy

# Pandas

# Matplotlib