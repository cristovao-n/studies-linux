# Command Basics

## Prompt

The terminal is ready to receive input and it is listening and waiting for a command.  
If you’re not seeing the prompt, it means that bash isn’t ready to receive your commands

**Case Matters**: Commands are case sensitive, so Date isn’t the same thing as date  
If you’re using OX S, some commands aren’t case sensitive, but others are. It’s safest to assume all commands are case sensitive.

## Command Structure

`command -options arguments`

Most commands support multiple options that modify their behavior.  
Many commands accept arguments

### Arguments

The order of the arguments matter

### Options

Options modify the behavior of the command in predefined ways  
Options are prefixed by a dash

Case matters`ncal -b` != `ncal -B`

We can provide multiple options at once  
Example:  
`ncal -3 -h -j -M` --> `ncal -3hjM`

#### Long Form Options

**Some** options support equivalent long format options  
These long form options are prefixed with two dashes instead of just one
Example:  
`date -u` --> `date --universal`  
`sort -ru colors.txt` --> `sort --reverse --unique colors.txt`

#### Options with Parameters

Some options require us to pass in an additional value  
Example:  
`ncal -A 1` or `ncal -A1`  
`ncal -B 2` or `ncal -B2`  
`ncal -A1 -B1 may 2003`







Clears the terminal  
`clear`

Shows the current date  
`date`

Show the calendar of the current month horizontally (calendar)  
`cal may 2003`

Show the calendar of the current month vertically (new calendar)  
`ncal 2003`

Takes the arguments we provide and prints them out (it echoes back to us)  
`echo $JAVA_HOME`

Prints out the sorted content of the file provided by argument  
`sort colors.txt`

Replace a single-line text  
`sed s/(regex-group)/\1/g`

Replace a multi-line text  
``

> More about **tr** and **sed**:
>
> [How can I replace each newline (\n) with a space using sed?](https://stackoverflow.com/questions/1251999/how-can-i-replace-each-newline-n-with-a-space-using-sed)
