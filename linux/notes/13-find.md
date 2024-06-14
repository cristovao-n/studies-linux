# Find

### Important

-   find command basics

### Useful

-   locate command
-   understanding timestamps
-   finding by time
-   find w/ exec
-   xargs command

## locate

The `locate` command performs a search of pathnames across our machine that match a given substring and then prints out any matching names  
It's nice and speedy because it uses a pre-generated database file rather than searching the entire machine  
You can use the pathname expansion wildcards, but the correct path must be used for the expansion to work

`locate PATTERN`

## Timestamps

### mtime

Modification time: when a file was last modified, when its contents last changed  
Can be seen using `ls -l`

### ctime

Change time: when a file was last changed. This occurs anytime mtime changes but also when we rename a file, move it, or alter permissions  
Can be seen using `ls -lc`

### atime

Access time: it's updated when a file is read by an application or a command like cat  
Can be seen using `ls -lu`

## find

The `find` command list every single file and directory recursively  
It does not use a database file, so it's slower but it's far more powerful

`find DIRECTORY`

### type option

Search only files  
`find -type f`

Search only directories  
`find -type d`

### Finding by name

-   name option

Find by name pattern  
`find ~/Desktop -name "*.txt"`

Case insensitive  
`find ~/Desktop -iname "*chick*"`

### Finding by size

-   size option

Find all files larger than 1 gigabyte  
`find -size +1G`

Find all files under 50 megabytes  
`find -size -50M`

Find all files that are exactly 20 kilobytes  
`find -size 20k`

### Finding by owner

-   user option

Find files and directories that belong to a particular user  
`find -user cristovao`

### Finding empty objects

-   empty option

Find empty files  
`find -empty -type f`

Find empty directories  
`find -empty -type d`

### Finding by timestamps

#### Options pattern

`find -[amc](min|time) [+-]*[0-9]+`

Modified exactly 30 minutes ago  
`find -mmin 30`

Accessed more than 30 minutes ago  
`find -amin +30`

Changed less than 30 minutes ago  
`find -cmin -30`

Modified less than 5 days ago  
`find -mtime -5`

Changed more than 10 days ago  
`find -mtime +10`

### Logical Operators

We can also use `-and`, `-or` and `-not` operators to create more complex queries

`find -name "*chick*" -or -name "*kitty*"`
`find -type -f -not -name "*.html"`

### User-defined actions

We can provide `find` with our own action to perform using each matching pathname

`find -exec COMMAND '{}' ';'`

The `{}` are a placeholder for the current pathname (each match) and the semicolon is required to indicate the end of the command

Usage  
`echo 'find ~ -type f -empty -exec ls -l '{}' ';'`

Renaming files  
`find -type f ! -empty -exec cp '{}' '{}_BACKUP' ';'`

> OBS: use `-ok` instead of `-exec` to get a confirmation prompt for each iteration

## xargs

The `xargs` command builds up the input into a bundle that will be provided as an argument list to the next command

Usage  
`echo hello world | xargs mkdir`
