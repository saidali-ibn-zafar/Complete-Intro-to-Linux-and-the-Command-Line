# Permission shortcuts

To set group permissions using symbolic notation, we can use the following symbols:

`r`: Read permission 

`w`: Write permission

`x`: Execute permission

Here's how we can set group permissions using symbolic notation:

`+`: Adds the specified permissions.

`-`: Removes the specified permissions.

`=`: Sets the specified permissions, overwriting any existing permissions.

For example, if we have a file named `example.txt` and we want to give the group write permission, we can use the chmod command like this:

```bash
chmod g+w example.txt
```

This command adds `write (w) permission` for the group (g) to the file `example.txt`.

Similarly, if we want to remove execute permission for the group, we can use:

```bash
chmod g-x example.txt

```

And if we want to set only read and execute permissions for the group, we can use:

```bash
chmod g=rx example.txt

```


- - - - - 

### Running `chmod 777 file.txt` sets the permissions of the file named `file.txt` to allow full read, write, and execute access for the owner, group, and all other users.

Here's what each digit in chmod 777 represents:

The first digit `(7)` sets the permissions for the `owner` of the file (file.txt).

The second digit `(7)` sets the permissions for the `group` that owns the file.

The third digit `(7)` sets the permissions for all `other users` (not the owner and not in the group).

### In `Unix` file permissions:

`4` represents `read` permission.

`2`represents `write` permission.

`1` represents `execute` permission.

### Adding these values together allows us to set the desired permissions. With `chmod 777`, each digit is set to the `sum of the permissions`:

`Owner` has `rwx (4 + 2 + 1 = 7)` permissions.

`Group` has `rwx (4 + 2 + 1 = 7)` permissions.

`Others` have `rwx (4 + 2 + 1 = 7)` permissions.
