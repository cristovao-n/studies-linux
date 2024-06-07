# Command Basics

## Prompt

The terminal is ready to receive input and it is listening and waiting for a command.  
If you’re not seeing the prompt, it means that the machine isn’t ready to receive your commands

**Case Matters**: Commands are case sensitive, so Date isn’t the same thing as date  
If you’re using OX S, some commands aren’t case sensitive, but others are. It’s safest to assume all commands are case sensitive.

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
