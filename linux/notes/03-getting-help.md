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

### Manual Sections

There are 8 sections which the man pages are organized

Search for a man:  
`man -k MAN_NAME`

Open a man in a specific section:  
`man SECTION_NUMBER passwd`

## help

Sometimes the command does not have a page in `man`  
When it happens, you can see it's available in `help`  
`help pwd`

## type

The type command will tell us the type of a command

There are four types of commands:

-   An executable program, usually stored in `/bin`, `/usr/bin` or `/usr/local/bin`. These are compiled binary files
-   A built-in shell command. These commands are part of the shell (bash in our case)
-   A shell function
-   An alias

Usage:  
`type COMMAND`

## which

Find the exact location of an executable:  
`which COMMAND`

This only works for executables, not built-in shell commands or aliases

## less

The man pages and git log command are opened by default with a tool called `less`

Usage:  
`less INPUT`

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
