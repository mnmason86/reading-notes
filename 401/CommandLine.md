[<=== Back](../README.md)

# Practice in the Terminal

Resource for working with the Bash Command Line

[The Command Line](https://ryanstutorials.net/linuxtutorial/commandline.php)   

### The Command Line

- Use `echo $SHELL` to view your current shell, it should end in `bash`.
- Recent history is stored and can be accessed using the up and down arrow keys.

### Basic Navigation

- The difference between Absolute and Relative paths
  - Absolute paths are in relation to the *root* directory and always begin with `/`.
  - Relative paths are in relation to where we are currently working in the system, and do not begin with a slash.

### More About Files

- Remember that *everything* is a file!
- If there is a space in a file name, quotation marks or the escape character `/` can be used to access that file.

### Manual Pages

- To view an explanation of a command in the terminal, use `man <command>`
  - This will display information about the command, how it is used, and what arguments it accepts.
  - To search *for* a manual page, use `man -k <search term>`
  - To search *within* a manual page, use `/<term>`, cycle through instances with the 'n' key.

### File Manipulation

- A few useful options to remember for `mkdir`:
  - `mkdir p` tells `mkdir` to make parent directories as needed.
  - Adding `-v`, will cause `mkdir` to confirm what it is doing.
- `-rmdir <directory>` will remove a directory, but it must be empty first.
- `rm -r` will remove a directory and all files and directories contained within it (use with caution!)

### [Cheat Sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)   
