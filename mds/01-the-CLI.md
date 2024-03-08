# What is `CLI`?

### A command-line interface (CLI) is a means of interacting with a computer program by inputting lines of text called command-lines. 

- - - - - 

## cd

The `cd` command in Linux stands for `"change directory."` It's used to change the current working directory in the terminal.

```bash

cd /path/...
```

## ls

The `ls` command in Linux stands for `"list."` It is used to list the contents of a directory. When we execute ls without any arguments, it will display the contents of the current directory.

```bash

ls
```

```bash
ls arg
```

The command `ls -lash` is used to list detailed information about files and directories in a directory.

## pwd

The `pwd` command in Linux stands for `"print working directory."` It is used to display the current working directory. 

```bash
pwd
```

## help

In a Linux terminal, we can typically get help for commands by using the `--help` option or by using the man command followed by the name of the command we want help with.

```bash
ls --help
```

or

```bash
man ls
```

## echo

In Linux, the `echo` command is used to display text or variables to the terminal. It's commonly used in shell scripts or directly in the command line to print messages or display the values of variables.

```bash
echo "Hello, World!"
```

### which

The `which` command in Linux is used to locate the executable file associated with a given command. It helps us to determine the full path of the executable file that will be executed when we run a command in the terminal.

```bash
which ls
```

This command will output the full path to the `ls` command, such as `/bin/ls`.

### touch

The `touch` command in Linux is used to create an empty file or update the access and modification timestamps of an existing file. It is often used to create new files quickly or to update the timestamps of files.

```bash
touch filename.txt
```

```bash
touch file1.txt file2.txt file3.txt
```

- - - - - - 

# flags

In Linux, `"flags"` generally refer to the various options or parameters that can be passed to commands or programs to modify their behavior. These flags are also known as command-line options, switches, or arguments.

- Single-letter flags, like -l, -a, -h, etc.
- Multi-letter flags, like --help, --version, etc.
- Some flags can also take arguments, for example, in cp command, the -r flag for recursively copying directories requires an argument specifying the source directory.

### dash - 

One dash is a shortcut like: 

```bash
-a
```

two dash is a long of doing it: 

```bash
--all
```

### ~ 

In Linux, the tilde `(~)` character is a shorthand representation of the current user's home directory. When used in a command or path, it refers to the home directory of the currently logged-in user.

### man

`man` is a command used in Unix and Unix-like operating systems (such as Linux) to display the manual pages for various commands and utilities.

The `man` command stands for `"manual"`

For example, if we want to learn more about the `ls` command, we can type man ls in the terminal, and it will display the manual page for the `ls` command, which includes information on how to use it, what options are available, and examples of its usage.

### cat

The `cat` command is a commonly used command-line utility in Unix-like operating systems. Its primary purpose is to concatenate and display the contents of files. However, it can also be used to create new files, concatenate multiple files together, and display non-printing characters.

Display the contents of a file:

```bash
cat filename

```

Concatenate multiple files and display the result:

```bash
cat file1 file2 file3

```

### tail 

`tail` displays the last few lines of a text file. By default, it shows the last `10` lines, but you can change this.

```bash
tail filename
```

## head

The `head` command displays the first few lines of a text file. It defaults to showing the first 10 lines but can be adjusted as needed.

```bash
head -n 3 fileName.txt
```

it will give us 3 lines from the beginning.

And same thing with tail as well!!!
