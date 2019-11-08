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
   
   chown -R username filename

   - Change Mode : `chmod`

     
