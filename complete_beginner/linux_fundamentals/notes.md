# Linux Fundamentals
## A Bit of Background on Linux
Linux is a command line operating system based on unix. The first release of the Linux operating system occurred in 1991. There are multiple operating systems that are based on Linux. It is actually an umbrella term for multiple OS's that are based on UNIX. Because UNIX is open-source, there are various flavors of Linux which each suit best for what the system is being used for. Ubuntu & Debian, for example, are some of the more commonplace distributions of Linux because it is so extensible. Ubuntu can be run as a server for websites/web applications or it can be used as a fully-fledged desktop.

## First Few Commands
| Command | Description |
| --- | --- |
|echo | Output any text that we provide to the terminal |
| whoami | Find out what user we're currently logged in as |
| ls | Used to list all the files in the current working directory |
| cd | Change directory |
| cat | Concatenate file |
| pwd | Print current working directory |
|find | Search current working directory by default, if directory is not defined, and all of it's sub-directories |

When utilizing the 'find' command, we are able to be more specific with our search.

In order to search the whole filesystem, the command should begin with 'find /'.

There are 2 very useful flags that we could use along with our 'find' command:

| Flag | Description |
| --- | --- |
| -type | You are able to add 'd' for directories or 'f' for files.|
| -name | Is used to specify a name or pattern to look for |
| -iname | Similar to the '-name' flag, but this is case sensitive |

i.e. In order to find all files whose name ends with ".xml", we will use the following script:
```
find / -type f -name "*.xml"
```
---
## Downloading Files
The **wget** command allows the user to download files from the web via HTTP &mdash; as if you were accessing the file in your browser. The user would just need to provide the accress of the resource that they wish to download. Example shown below:
```
wget https://assets.tryhackme.com/additional/linux-fundamentals/part3/myfile.txt
```

## Transferring Files From Your Host - SCP (SSH)
Secure copy, or SCP, is just that &mdash; a means of securely copying files. Unlike the regular cp command, this command allows you to transfer files between two computers using te SSH protocol to provide both authentication and encryption.

Working on a model of SOURCE and DESTINATION, SCP allows the user to:
* Copy files & directories from your current system to a remote system
* Copy files & directories from a remote system to the current system

## Viewing Processes
We can use the **'ps'** command to provide a list of the running processes as our user's session and some additional information such as its status code, the session its running in, how much time of the CPPU it is using, and the name of the actual program or command that is being executed.

In order for us to see the processes run by other users and those that don't run from a session, we need to provide **aux** to the ps command:
```
ps aux
```

