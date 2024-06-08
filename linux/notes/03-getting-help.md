# Getting Help

There are available tools in bash to help us with the documentation of the commands

For example, if we see this command: `ncal -w` how would we know what the `w` option mean?

## man

The man pages, short for manual pages, are a built-in form of documentation available on nearly all Unix-like operating systems

The specific contents vary from one operating system to another, but at a base minimum the man pages include information on commands and their usage

Usage:  
`man echo`

### Synopsis

`ncal [-31bhJeoSM] [-A number] [-B number] [-d yyyy-mm] [year]`  
`cp [OPTIONS]... SOURCE DEST`  

Anything listed inside of square brackets is optional.  
The ellipsis indicates that one or more of the proceeding operand are allowed

## less

The man pages are opened with a tool called `less`

Get help  
`h`

Go to next page  
`f`

Go to previous page  
`b`

Search next occurrence  
`/pattern`

Search previous occurrence  
`?pattern`

Other options:  
`help cd`  
`info cd`
