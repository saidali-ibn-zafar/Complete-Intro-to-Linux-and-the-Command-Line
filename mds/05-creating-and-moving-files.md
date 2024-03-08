# creating and moving files

### remove (rm)

⚠️Be cautious when using the `rm` command as it permanently deletes files and directories, and there's usually no way to recover them once they're removed. 

To delete a file:

```bash
rm filename
```

To delete a directory and its contents recursively:

```bash
rm -r directoryname
```


This command below will delete the specified directory and all its subdirectories and files, including hidden files, without asking for confirmation.

```bash
rm -rf directoryname

```

The command `rm -rf *` is one of the most dangerous commands in Unix-like operating systems. It recursively deletes all files and directories in the current directory without asking for confirmation.

```bash
rm -rf *
```

### copying (cp)

The `cp` command in Unix-like operating systems is used to copy files and directories.

```bash
cp source_file destination_file

```

The `cp -R` command is similar to `cp -r` and is used to copy directories and their contents recursively. 

```bash
cp -R source_directory destination_directory

```
