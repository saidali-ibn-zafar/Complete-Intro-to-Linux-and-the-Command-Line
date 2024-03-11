# shell script

### A shell script is a script written for a shell, which is a command-line interpreter for Unix-like operating systems. The shell is a program that takes commands from the keyboard and gives them to the operating system to perform. Shell scripts allow us to automate tasks by writing a series of commands in a text file, which can then be executed as a single program.

```bash
#!/bin/bash

# This is a simple shell script that prints "Hello, world!" to the terminal.

echo "Hello, world!"

```

We can create a new file using a text editor, such as `nano`, `vim`, or `gedit`.

Save the file with a `.sh` extension, for example, `hello_world.sh`.

Make the script executable by running `chmod +x hello_world.sh` in the terminal.

Finally, execute the script by typing `./hello_world.sh` in the terminal.

- - - - - 

# variables



```bash
#!/bin/bash

# Initialize variables
name=""
age=0

# Main script starts here
echo "Initializing variables..."
name="John Doe"
age=30

echo "Name: $name"
echo "Age: $age"

```

We initialize the variables `name` and `age` to empty values.

Then, we assign values to these variables `("John Doe" and 30, respectively)` to simulate initializing them with user data.

Finally, we print the values of these variables to confirm that they have been initialized correctly.

- - - - -

# arguments

### In shell scripting, arguments are values provided to a script or a function when it is called or invoked. These arguments can be passed to the script or function from the command line or from within another script.

Positional parameters are variables that hold the arguments passed to the script.

They are represented by numbers starting from `$1`, `$2`, `3`, and so on, up to `$9`.

`$0` represents the script's name itself.

`$#` holds the total number of arguments passed.

```bash
#!/bin/bash

echo "Script name: $0"
echo "First argument: $1"
echo "Second argument: $2"
echo "Total number of arguments: $#"

```

If we run this script with command line `arguments like ./example.sh arg1 arg2`, it will output:

```bash
Script name: example.sh
First argument: arg1
Second argument: arg2
Total number of arguments: 2

```

- - - - - - 

# read

```bash
#!/bin/bash

# Prompt the user for input and store it in the variable
read -p "Enter your name: " nameOfVariable

# Print the value of the variable
echo "Hello, $nameOfVariable!"

```

- - - - -

# conditionals : if statements

### In shell scripting, conditional statements are used to execute certain code blocks based on whether a given condition evaluates to true or false. The most commonly used conditional construct in Bash is the if statement.

```bash
if [ condition ]; then
    # code block to execute if the condition is true
fi

```

### example: 

```bash
#!/bin/bash

# Define a variable
number=15

# Check if the number is greater than 10
if [ "$number" -gt 10 ]; then
    echo "The number is greater than 10."
fi

```

- - - - - 

# comparison operators: 

`-gt`: Greater than

`-eq`: Equal to

`-lt`: Less than

`-ge`: Greater than or equal to

`-le`: Less than or equal to

`-ne`: Not equal to

## for more try this `man test`

- - - - - 

In Bash scripting, you can use the `if`, `elif` (short for "else if"), and else statements to implement conditional logic. 

```bash
#!/bin/bash

# Define a variable
number=15

# Check conditions using if, elif, and else
if [ "$number" -gt 10 ]; then
    echo "The number is greater than 10."
elif [ "$number" -eq 10 ]; then
    echo "The number is equal to 10."
else
    echo "The number is less than 10."
fi

```

- - - - -  

# arrays


In Bash scripting, arrays are used to store multiple values under a single variable name. 

```bash
#!/bin/bash

# Declare an array named "my_array"
my_array=(apple banana cherry)

```

```bash
# Access the first element of the array
echo "${my_array[0]}"  # Output: apple

# Access the second element of the array
echo "${my_array[1]}"  # Output: banana

# Access the third element of the array
echo "${my_array[2]}"  # Output: cherry
  
```

### array length

```bash
# Get the length of the array
length=${#my_array[@]}
echo "Array length: $length"  # Output: 3

```

- - - - - -

# loops

### for loop

```bash
#!/bin/bash

# Syntax for iterating over elements in an array
for item in "${array[@]}"; do
    # Commands to execute for each item
    echo "$item"
done

# Syntax for iterating over a sequence of numbers
for (( i=0; i<5; i++ )); do
    # Commands to execute for each iteration
    echo "$i"
done

```

### while loop

```bash
#!/bin/bash

# Syntax for a while loop
while [ condition ]; do
    # Commands to execute as long as the condition is true
    echo "Condition is true"
done

```

### until loop

```bash
#!/bin/bash

# Syntax for an until loop
until [ condition ]; do
    # Commands to execute until the condition becomes true
    echo "Condition is false"
done

```
