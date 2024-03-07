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
