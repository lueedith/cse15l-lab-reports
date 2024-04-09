  1. cd ran with No Arguments

![Image](1.png)
Output: (No visual output, but it changes the working directory to the user's home directory)
Explanation: Running cd with no arguments defaults to changing the working directory to the user's home directory. In this case, it changed from /user/lueedith/lecture1 to /user/lueedith.
Error: No

2. cd ran with Path to a Directory

  Command: cd lecture1
  Absolute Path Before Command: /user/lueedith
  Output: (No visual output, directory changes to specified path)
  Explanation: The command changes the working directory to the specified path. projects/lab1 is a directory inside /home/user, so the new working directory is /home/user/projects/lab1.
  Error: No
  
3. cd ran with Path to a File (Error)

  Command: cd readme.txt
  Absolute Path Before Command: /home/user/projects/lab1
  Output: bash: cd: Hello.java: Not a directory
  Explanation: The cd command is used to change directories, not to open files. Since readme.txt is a file, not a directory, the command fails with an error.
  Error: Yes
  
4. ls ran with No Arguments

  Command: ls
  Absolute Path Before Command: /home/user/projects
  Output: Hello.class Hello.java README messages
  Explanation: Displays the contents of the current directory, in this case the contents of lecture1 directory.
  Error: No

5. ls ran with Path to a Directory

  Command: ls lab1
  Absolute Path Before Command: /home/user/projects
  Output: exercise1.txt exercise2.txt
  Explanation: Lists the contents of the lab1 directory, showing two text files.
  Error: No

6. ls ran with Path to a File

  Command: ls readme.txt
  Absolute Path Before Command: /home/user/projects
  Output: readme.txt
  Explanation: Lists the specified file, confirming its presence in the directory.
  Error: No

7. cat ran with No Arguments (Error)

  Command: cat
  Absolute Path Before Command: /home/user/projects/lab1
  Output: cat: missing file operand
  Explanation: The cat command requires at least one file name as an argument to display its contents. Without any arguments, it returns an error.
  Error: Yes

8. cat ran with Path to a Directory (Error)

  Command: cat lab2
  Absolute Path Before Command: /home/user/projects
  Output: cat: lab2: Is a directory
  Explanation: The cat command is intended for displaying file contents, not directory contents. Thus, using it on a directory returns an error.
  Error: Yes

9. cat ran with Path to a File

  Command: cat readme.txt
  Absolute Path Before Command: /home/user/projects
  Output: This is the README file for the projects directory.
  Explanation: Displays the contents of readme.txt, which is a brief description of the directory.
  Error: No
