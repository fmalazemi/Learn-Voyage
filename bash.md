### find
- `find . -name fileName` 
- `find /home -user exampleuser -mtime 7 -iname ".db`   ---- Find all .db files (ignoring text case) modified in the last 7 days by a user named exampleuser.

### grep (search a file for a pattern)
- `grep -rnw 'PATH' -e 'pattern'`
  - `-r` recursive 
  - `-n` show line number in output
  - `-w` match the whole word
  - `-i` ignore case
  - `-e` pattern you would like to search 
  - `PATH` start from this path

### pgrep (look up or signal processes based on name and other attributes)
- `pgrep P_NAME` --- print process IDs that include "P_NAME" in the command. Each on a seperate line. 
- `pgrep -d "," P_NAME"` --- print process IDs that include "P_NAME" in the command. Concatinate ID with ",". 

### top 
- `top -p PID` --- show statistics and usage information related to PID only. 
- ``top -p `pgrep -d "," P_NAME` `` --- Show processes that include "P_NAME" in the command.  
- `top -U username` --- qShow processes currently running by the 
### scp 
- `scp [sourceUser@SourceAddreess]:SourcePath [destUser@destAddress]:destPath` 
- `scp user@xyz.com:/scratch/dump.txt .` --- copy file dump.txt from xyz.com server to current working directory. 
### screen 
This command helps to open a new shell that can be active and running even after user logs out. 
- `screen` -- open a new shell
- `screen -r [PID]` --- resume a currently running shell, if more than one screen shell is running select specific PID. 
- `screen -d` --- detach the current working screen and back to parent shell prompt. 
### output redirection
- `command > file` --- if file does not exists, create and redirect output. If file exists, raise an exception. 
- `command >> file` --- if file exists append, o.w. create a new file. 
- `command >! file` --- Delete the content of the file and redirect the output. 

### Disk space usage
- `du`
  - `-s` --- summarize disk usage for the current working directory. 
  - `-h` --- convert disk space to humen format (e.g. 1GB)
  - `-c` --- Sum all calculated disk usage and print total on the last line.  
- `du -csh .` --- example: calculate disk usage of all files and dir in '.' directory and print total at the end.  
