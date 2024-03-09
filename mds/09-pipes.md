# Pipes

When we run `cat fileName.txt | grep "hello"`, it effectively `searches` for the word `"hello"` in the contents of the `fileName.txt` file and `prints` out any lines containing that word.

```bash
cat fileName.txt | grep "hello"

```


We can also use wildcards with `rm -i` to delete multiple files while being prompted for confirmation for each one:

```bash
rm -i *.txt
```

In these codes below we are removing all the txt files and it is `y` - `yes` for the confirmation.

```bash
yes y | rm -i *.txt
```

opposite one is 

```bash
yes n | rm -i *.txt
```
