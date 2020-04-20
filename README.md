## Lesson 2.1

 - Print working directory  
`pwd`

 - Current user name  
`whoami`

 - List files or directories  
`ls`
`ls -l`

 - Current ip address configuration  
`ip addr show`

 - Free memory  
`free -m`

 - Disk free  
`df -h`

 - Show the contents of a file  
`cat /etc/hosts`

 - Show mounted filesystems as a tree   
`findmnt`

## Lesson 2.2
 - Commands history  
`history`

 - Run command number in history  
 runs command number 11  
`!11` 

 - Runs last command that starts with "f"  
`!f`

  - Search in history  
`Ctrl + R`

 - Piping examples  
`ps aux | less`
`ps aux | wc`

 - Redirection example  
`ls > lsfiles`

 - Redirection operators  
`>` rewrite file  
`>>` append to a file

 - Redirect error message 2> to a file named "errors"  
`ls lwiedwqdq 2> errors`

 - Shows only the valid results  
`ls dwqdwqq * 2> /dev/null`

 - Environment variables  
`env`

 - Set enviornment variable  
`LANG=fr_FR.utf-8`

 - Show aliases  
`alias`

 - Set an alias  
`alias h=history`

## Lesson 2.3

Standard input: `file < command` The File will be used as input to a command
Standard output: `command > file` Overwrite
Standard output: `command >> file` Append
Standard error: `2>`
 
## Lesson 2.4

 - Ignore errror messages  
`grep -R student /etc 2>/dev/null`

 - Piping  
`ls -l /etc | grep host`

## Lesson 2.5 - Understanding the Linux Filesystem Hierarchy (FHS)

`/etc` - config fils  
`/boot` - kernel  
`/home` - users  
`/usr` - program files  
`/usr/bin` - programs usable by regular users  
`/usr/sbin` - programs usable by root user (super users)  
`/var` - dynamic data  
`/var/log` - log files  

 - Description of filesystem hierarchy  
`man hier`

## Lesson 2.6 - Using man

 - How to use man  
`man man`

## Lesson 2.7

 - Search man db
`man -k user`

## Lesson 2.9 - vim

 `i, a` - insert, append  
 `o` - new line, insert mode  
 `:wq` - save and quit  
 `:q!` - quit without asking to save  
 `dd` - delete current line  
 `yy` - copy the current line  
 `p` - paste  
 `d$` - delete from the current cursor position to the end of the line  
 
 `v` - visual mode - selecting text  
 `u` - undo  
 `Ctrl-R` - redo  

 `gg` - go to the top of the file  
 `G` - go to the end of the file  
 `/text` - search - downwards  
 `?text` - search upwards  
 `n` - repeat last search action  
 `^` - bring the cursor to the begining of the current line  
 `$` - bring the cursor to the end of the current line  
 `:%s/old/new/g` - global substitute; without the "g" only one replacement  

## Lesson 2.10 - Globbing and Wildcards

`man 7 glob`

 - Example  
ls host*

 - Single character - `?`  
`ls ?ost`

 - Start with one of the characters h or m  
`ls [hm]ost`

 - Not starting witch h or m  
`[!hm]ost`

 - Ending with two digits  
`ls script[0-9][0-9]`

 - Testing - create multiple files  
`touch script{0..100}`

## Lesson 2.11 - Cockpit

`systemctl enable --now cockpit.socket`  
`systemctl status cockpit.socket`
