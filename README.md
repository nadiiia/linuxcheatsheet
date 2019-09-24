Linux cheat sheet

# SSH

ssh command consists of 3 different parts:
+ ssh command instructs the system to establish an encrypted secure connection with the host machine.
+ user_name represents the account that is being accessed on the host.
+ host refers to the machine which can be a computer or a router that is being accessed. It can be an IP address (e.g. 192.168.1.24) or domain name(e.g. www.domainname.com).

```shell script
ssh user_name@host(IP/Domain_name)
```

``` shell script
ssh-keygen
```

# cat
``` shell script
cat [OPTION] [FILE]...
```

+ display contents of file
+ view contents of multiple files 

``` shell script
 cat file1 file2
```     
+ create file

 ``` shell script
cat >filename 
   ```
+ to limit preview of content
 ```shell script
cat file | more
 ```
``` shell script 
cat file | less 
 ```
 + display line number in file
 ``` shell script 
cat -n filename   
  ```
    
   + display $ (end of line) in file
   
 ``` shell script 
cat -e filename 
  ```
 + display tab separated lines in file
   
 ``` shell script 
 cat -T filename 
  ```
+ display multiple  files
   
 ``` shell script 
cat filename0; cat filename1; cat filename2
  ```
+ standard output with redirection 

Standard output of a file can be added into a new file or existing file with ‘>‘ (greater than) symbol. Careful, existing contents of test1 will be overwritten by contents of test file.
   
 ``` shell script 
cat test0 > test1
  ```
  
  similarly contents of multiple can be added into single file (new or existing)
  
   ``` shell script 
cat test0 test1 test2 > testN 
  ``` 
 + Appending standard output with redirection 

The contents of test file will be appended at the end of test1 file.
   
 ``` shell script 
cat test0 >> test1
  ```
+ Sorting Contents of Multiple Files in a Single File

This will create a file test4 and output of cat command is piped to sort and result will be redirected in a newly created file.
   
 ``` shell script 
cat test0 test1 test2 test3 | sort > test4
  ```
# Copying, moving, removing files

+ to make a copy of file1 in the current working directory and call it file2
``` shell script
cp file 1 file2
```
+ to move or rename  file1 to file2
``` shell script
mv file 1 file2
```  
 +  to remove file use the following
 ``` shell scrip
  rm [OPTION]... FILE...
```

 +  to remove empty directories from the filesystem 
 ``` shell scrip
  rmdir [-p] [-v | –verbose] [–ignore-fail-on-non-empty] directories …..
```

# Special characters

+  **-**

if filename is **-** (dash), you simply need to give can some indication that you want a litteral file of that name, not the internal alias it has. You can do this easiest by specifying a path to the file
``` shell script
cat ./-
```
+  **#**  Pound/hash

Line beginning with **#** will not be executed. Used  as a comment. 
+  **;**  Semicolon

Command separator [semicolon]. Permits putting two or more commands on the same line.

+  **.**  Dot

 When working with filenames, a leading dot is the prefix of a "hidden" file, a file that an ls will not normally show.
 
 When considering directory names, a **.** (single dot) represents the current working directory, and **..** (two dots)  denote the parent directory.
 
 When matching characters, as part of a regular expression, a "**.**" matches a single character. 
 
 +  **\\**  Backslash
 
 A quoting mechanism for single characters.
 
  +  Space (in a filename)
 
  ``` shell script
 cat "file name with space"
```
or 
 ``` shell script
 cat file\ name\ with\ space
```

# Useful commands

+   pwd

 print path of the working directory 
+   ls 

It is used to list information about files and directories within the file system.
 ``` shell script
ls [OPTIONS] [FILES]
```
| option     | description        |
| ------------- |:-------------:| 
|ls -a      | list all files including hidden file starting with '.' | 
| ls --color     | colored list [=always/never/auto]    |
| ls -d  | list directories - with ' */'    |
| ls -F | add one char of */=>@| to enteries     |
| ls -i  |list file's inode index number      |
| ls -l| list with long format - show permissions     |
| ls -la  | list long format including hidden files    |
| ls -lh | list long format with readable file size      |
| ls -ls |list with long format with file size     |
| ls -r |list in reverse order   |
| ls -R |list recursively directory tree   |
| ls -s |list file size    |
| ls -t |sort by time & date   |
| ls -X |sort by extension name    |	
 	
 List root directory:

 ``` shell script
 ls /
````


List parent directory:
 ``` shell script
 ls ..
````

List user's home directory (e.g: /home/user):

 ``` shell script
 ls ~
````

List all subdirectories:

 ``` shell script
 ls *
```
+ find
 ``` shell script
find [where to start searching from]
 [expression determines what to find] [-options] [what to find]
 ```
 + grep
 
 ``` shell script
 grep [options] pattern [files]
  ```	
| option     | description        |
| ------------- |:-------------:| 
|-c      | This prints only a count of the lines that match a pattern| 
| -h    | Display the matched lines, but do not display the filenames.   |
| -i  | Ignores, case for matching |
| -l  | Displays list of a filenames only.    |
|-n   |Display the matched lines and their line numbers. |
| -v | This prints out all the lines that do not matches the pattern    |
| -e  exp| Specifies expression with this option. Can use multiple times.   |
| -f file| Takes patterns from file, one per line    |
| -E |Treats pattern as an extended regular expression (ERE)    |
| -w |Match whole word   |
| -o |Print only the matched parts of a matching line, with each such part on a separate output line. 	   |

