# Wildcards and Replacements

## `{}` notation to perform replacements when creating files with the `touch` command.

### creating multiple files

To create multiple files with a similar naming pattern using the `touch` command, we can use curly braces `{}` to specify the variations in the filenames. 

For example, to create files named `file1.txt`, `file2.txt`, `file3.txt`, `file4.txt`, and `file5.txt`, we can use the following command:

```bash
touch file{1,2,3,4,5}.txt
```


To create files named `file-ca.txt`, `file-nm.txt`, and `file-.txt`, we can use the following touch command:

```bash
touch file-{ca,nm,}.txt
```

##  Wildcards allow us to select multiple files or directories based on matching criteria. Here are some commonly used wildcards:

 - `*` (asterisk): Matches any sequence of characters (including zero characters).
 - `?` (question mark): Matches any single character.
 - `[ ]` (square brackets): Matches any single character within the specified range or set.
 - `[^ ]` (caret inside square brackets): Matches any single character NOT within the specified range or set.

`*.txt`: Matches all files with the `.txt` extension.

`file*`: Matches all files that start with `"file"`.

`file?.txt`: Matches files like `file1.txt`, `file2.txt`, etc., but not `file10.txt`.

`[abc]*.txt`: Matches files that start with `"a"`, `"b"`, or `"c"` and have a `.txt` extension.

`file[0-9].txt`: Matches files like `file1.txt`, `file2.txt`, etc., but not `file10.txt`.

`file[^0-9].txt`: Matches files like `file-a.txt`, `file-b.txt`, etc., but not `file1.txt`.

- 
`{1..30}` is a brace expansion syntax that generates a sequence from 1 to 30. When combined with the touch command, it creates files named `file1.txt` through `file30.txt`

```bash
touch file{1..30}.txt

```

Executing this command will create files named `file1.txt`, `file2.txt`, `...`, `file30.txt` in the current directory. Each file will have the `.txt` extension.

This works for `{a..z}` as well...

## echo {}

The brace expansion `{a..z}` with the `echo` command, it will simply display the generated sequence of characters from `'a'` to `'z'`.

```bash
echo {a..z}

```

Output: 

```bash
a b c d e f g h i j k l m n o p q r s t u v w x y z

```


The brace expansion `{a..z..2}` with a step of `2` generates a sequence of characters from `'a'` to `'z'`, skipping every other character. However, brace expansion with a step value is not supported in all shells, such as Bash.

```bash
echo {a..z..2}
```

Output: 

```bash
a c e g i k m o q s u w y

```

or 

```bash
```bash
echo {a..z..5}
```

Output:

```bash
a f k p u z

```
If we want to achieve a similar result of printing every `5th` character from `'a'` to `'z'`, we might need to use other programming constructs, such as a loop in Bash. Here's an example using a loop:

```bash
for ((i=0; i<=25; i+=5)); do
    printf "%s " $(echo {a..z} | cut -c $(($i+1)) )
done

```

- - - - 

```bash
echo {a..z}{1..5}

```
It gives us all the permutation {a..z} and {1..5}

Output:

```bash
a1 a2 a3 a4 a5 b1 b2 b3 b4 b5 c1 c2 c3 c4 c5 d1 d2 d3 d4 d5 e1 e2 e3 e4 e5 f1 f2 f3 f4 f5 g1 g2 g3 g4 g5 h1 h2 h3 h4 h5 i1 i2 i3 i4 i5 j1 j2 j3 j4 j5 k1 k2 k3 k4 k5 l1 l2 l3 l4 l5 m1 m2 m3 m4 m5 n1 n2 n3 n4 n5 o1 o2 o3 o4 o5 p1 p2 p3 p4 p5 q1 q2 q3 q4 q5 r1 r2 r3 r4 r5 s1 s2 s3 s4 s5 t1 t2 t3 t4 t5 u1 u2 u3 u4 u5 v1 v2 v3 v4 v5 w1 w2 w3 w4 w5 x1 x2 x3 x4 x5 y1 y2 y3 y4 y5 z1 z2 z3 z4 z5

```
