## Output streams

We all know that `echo` and we need to write an argument and then it will display that argument on the terminal or console.

However if we redirect it into some files then we will have : 

```bash
echo "Hello world" > newFile.txt
```

or 

```bash
echo "Hello world" 1> newFile.txt
```

then it does not display anyrhing instead it creates a file called `newFile.txt` with the contents of `"Hello world"`

After that 

```bash
cat newFile.txt
```

Output: 

```bash
Hello world
```

- - - - -

```bash
cat newFile.txt > anotherFile.txt
```

What is going on there? 

```bash
cat anotherFile.txt
```

Output: 

```bash
Hello world
```

As you understand we are just copying!

And now we have `>>` 

What is this?

```bash
echo "Hello wolrd" >> anotherFile.txt
```

We had `anotherFile.txt` and the content of it was `"Hello world"`

```bash
cat anotherFile.txt
```

Outout:

```bash
Hello world
Hello world
```

It means `>>` does not remove the content instead it appends new content in the end!

So, `>` is for creating or overwriting files with new content, while `>>` is for appending content to existing files without overwriting their contents.

