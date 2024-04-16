# Linux Tools
- There are many tools:
	1. Information Gathering
	2. Vulnerability Analysis
	3. Web Application Analysis
	4. Database Assessment
	5. Password Attack
	6. Wireless Attack
	7. Reverse Engineering
	8. Exploitation Tools 
	9. Sniffing & Spoofing
	10. Post Exploitation
	11. Forensics
	12. Reporting Tools
	13. Social Engineering
	14. System Services

# Linux Command Basics
- On linux the are over 100 commands. Each have their own options & arguments.
> What is command?

### ls / list directory
- Lists information about the files. (The current directory by default.)
> 		**SYNOPSIS**: **ls [option] … [file] …**
> 		**Example**: ls -l ................. Gives more information about the lists.
> 				ls -a ............... Shows hidden files too
> 				ls filename/foldername
> 				ls -R .............. Recursive

- We can also **combine** them, **ls -Rla**
- Linux hidden files start with **dot.**

### cd / change directory
- Its used to change working directory.
> 		**SYNOPSIS:** cd [directory]
> 		**Example:** cd ..
> 				cd ../..
> 				cd "folder_name"

- If the **folder_name** have space use " ".

### pwd / print working directory
- It prints the path of the working directory, starting from the root.
> 		**SYNOPSIS:** pwd [options]
> 		**Example:** pwd Desktop = /home/kali/Desktop

### echo
- Displays line of text/string that are passed as an argument.
> 		**SYNOPSIS:** echo [option] … [string]
> 		**Example:** echo "text"
- Can **write** texts into files.
> 		**Examples:** echo "text" > file.txt
- Can **add** texts (append).
> 		**Example:** echo "text" >>file.txt

### cat / head / tail / less
- Used to show the context of a file.
> 		**SYNOPSIS:** cat [file]

### touch
- Creates any kind of files only.
- Its empty file inside.
> 		**SYNOPSIS:** touch [file1]  [file2]  [file3] …

### mkdir / make directory
- Creates folders.
> 		**SYSOPSIS:** mkdir [foldername1]  [foldername2]  [foldername3] …
- Use " " when using folder with space between them.

### rm / remove
- Removes a file/folder.
> 		**SYSOPSIS:** rm [file1]  [file2]  [file3] …
> 		**Example:** rm -r [filename] ............ recursive (4 folders)
> 				rm -i [filename] ............ for prompt (ask)
> 				rm -f [filename] ............ force delete

- Can be used in combination like **rm -rf 'filename'**

### cp / copy

### mv / move

### grep / global search for regular expression
- The grep filter searches a file for a particular pattern of characters & displays all lines that contain that pattern.
> 		**SYNOPSIS:** grep [options]  pattern [files]
> 		**Example:** grep -i "search" file ............... case insensitive
> 				grep -c "search" file ............. count numbers
> 				grep -l "search" * .................. display file name
> 				grep -R "search" foldername ............ search text in folders
> 				grep -v "term" filename ..................... to display without this term
> 				grep -n "term" file ................................ to display the term find number

### wc / word count
- Used to find out number of lines, word count, byte & character count in the file.
> 		**SYNOPSIS:** wc [option] … [file] ...
> 		**Example:** wc grep_test.txt
> 				**OUTPUT:** 1 (line (-l))    13(word(-w))     59(byte(-c))    grep_test.txt

## Multiple Command Executions
### AND ( && ): 
- All commands will be executed if both are working without error.
### OR ( || ):
- The command will be executed if it have error or not.
### Piping ( | ):
- Helps to commands by using the output of the 1st command as the input for the next one.