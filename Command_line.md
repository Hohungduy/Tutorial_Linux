----------------------------------------------------------------------------------------
#Tutorial for command line
----------------------------------------------------------------------------------------

1. Job control - Start multiple programs

   `jobs` - Running program check

   `fg xxx` - bring job to foreground.

   `bg xxx` - bring job to background

2. Environment Variables
   
   Printing Environment Variables:

   `printenv`
   
   Set environment and export environment variables

   `variable_name=value`

   `export variable_name`

   Unset environment variables 

   `unset variable_name`

3. Redirection: Take the output of program and send it to a file

   - To collect the output of program into a file: `cmd > ttt.txt`
   
   - To append addtional data, use two symbol: `echo "conheo" >> ttt.txt`

4. Environment Variables as Parameters: Under Bash script, we can use environment variables as parameters on the command line.

   $Variable_name : iValue of variable 

5. Multiple command: Using `;` and `&&`

6. Backticks: Use backtick to treate as a command to be execited

   EX: kill `cat /var/run/named/named.pid`

7. Documentation Tools: `man`
   
   Ex: `man ls` ; `man 1 printf`

   Read about st

   Ex: `info ls` ; `info printf`

8. Files type and File Ownership and File Permissions

   - List file : ls
   
   |  Options for ls | Description                 |
   | --------------- | :-------------------------: |
   |      -l         | Long listing                |
   |      -a         |  All files                  |
   |      -t         | Order of last modified time |
   |      -r         | Reverse the listing         |
   |      -1         | Single-column listing       |
   |      -R         | Recursively file -de quy    |

   - Change ownership: `chown`
   
   | Letter |  Permission  |  Value  |
   | ------ | :----------: | :-----: | 
   |   r    |   Read       |    4    |
   |   w    |   Write      |    2    |
   |   x    |   Execute    |    1    |
   chown -R username filename

   - Change Mode : `chmod`

   When listing files or directories, you see the permissios in the first column of the output: Normal file (-); Directories (d); Symbolic links (1)

   | Letter |  Permission  |  Value  |
   | ------ | :----------: | :-----: |
   |   r    |   Read       |    4    |
   |   w    |   Write      |    2    |
   |   x    |   Execute    |    1    |

   | Letter |  Permission  |  Value  |
   | ------ | :----------: | :-----: | 
   |  ---   | No permission|    0    |
   | Letter |  Permission  |  Value  |
   | ------ | :----------: | :-----: | 
   |   r    |   Read       |    4    |
   |   w    |   Write      |    2    |
   |   x    |   Execute    |    1    |
   |  r--   | Read only    |    4    |
   |  rw-   |  R,W         |    6    |
   |  rwx   |  R,W,E       |    7    |
   |  r-x   |  R,E         |    5    |
   |  --x   | Execute only |    1    |

9. Copy file :`cp`

10. Move files : `mv`

11. Link Files : `ln`

12. Find files : `find`

13. File Compression : `gzip`

14. Create a Directory : `mkdir`

15. Remove a Directory : `rmdir`

16. Show Present working Directory : `pwd`

17. Pack the program : `tar`

18. Concatenate Files : `cat`

    Ex: `cat /etc/passwd`

    Ex: `cat /etc/passwd /etc/group`

    Ex: `cat /etc/passwd etc/group > users-and-group.txt` (Concatenate and output into file txt)

    Ex: `cat /etc/hosts >> users-and-groups.txt` (Append the contents of the file)

19. Display a File One Screen at a Time : more

20. Disk Utiliztion : du

21. Show the directory Location of a File : which

22. List processes : ps (PID)

23. Kill process : kill



  

    
