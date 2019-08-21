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

+ display contents fo file
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