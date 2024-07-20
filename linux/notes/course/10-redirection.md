# Redirection

### Important

-   Redirecting standard output
-   Redirecting standard input
-   Redirecting standard error

### Nice to have

-   Fancy shortcut syntax

standard input `0` -> COMMAND -> (standard output `1`, standard error `2`)

## Redirecting standard input

Some commands listen to standard input if no input file is provided  
Example: cat, sort

To pass the contents of a file to standard input, use the `<` symbol followed by the filename  
`COMMAND < FILENAME`  
`COMMAND 0< FILENAME`  
`cat < chickens.txt`

## Redirecting standard output

The redirect output symbol `>` tells the shell to redirect the output of a command to a specific file, overwriting its contents or creating it, instead of the screen.  
`date > output.txt`  
`date 1> output.txt`

### Appending

When we redirect output into a file using `>` any existing contents in the file are overwritten.  
To add new content to the end of the file, use `>>`  
`echo "hello" >> greeting.txt`  
`echo "world" >> greeting.txt`

## Redirecting standard error

By default, error messages are output to the screen, but we can change this by redirecting standard error.  
The standard error redirection operator is `2>`  
`cat NONEXISTENTFILE 2> error.txt`

### Appending

`cat idontexist 2>> error.txt`

## Putting it all together

Redirect standard error to the same location as standard output  
`ls docs > output.txt 2> output.txt`

Fancy syntax  
`ls docs > output.txt 2>&1`

Fancier syntax supported by newer versions of bash  
`ls docs &> output.txt`

