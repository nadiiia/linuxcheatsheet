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
     