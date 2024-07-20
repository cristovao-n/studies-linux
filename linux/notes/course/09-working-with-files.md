# Working with files

### Important

-   cat command
-   less command
-   head command
-   tail command
-   sort command

### Useful

-   wc command
-   fancy sort stuff

### Nice to have

-   tac command
-   rev command

## cat

Print the content of a file to the standard output  
`cat FILE...`

## less

The man pages and git log command are opened by default with a tool called `less`

Usage:  
`less FILE`

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

## tac

cat spelled backwards  
Concatenate and print files in reverse vertically  
`tac FILE...`

## rev

Concatenate and print files in reverse horizontally  
`rev FILE...`

## head

Prints a portion of a file, starting from the beginning of the file  
By default, it prints the first 10 lines of a file

`head FILE`

Change the number of lines  
`head -5 FILE`

Prints all except the last N number of lines  
`tail -n-2 FILE`

Print first N bytes  
`head -c5 FILE`

## tail

Works similarly to the head command, except it prints from the end of the file  
By default, it prints the last 10 lines of a file

`tail FILE`

Change the number of lines  
`tail -5 FILE`

Prints all except the first N number of lines  
`tail -n+2 FILE`

Print last N bytes  
`tail -c5 FILE`

Listen file changes and output then (Useful to monitor logs)  
`tail -f FILE`

## wc

The word count command can tell us the number of words, lines or bytes in files  
By default, it prints out three numbers: the lines, words and bytes in a file  
`wc FILE`

Number of lines  
`wc -l FILE`

Number of words  
`wc -w FILE`

Number of characters  
`wc -m FILE`

Number of bytes  
`wc -c FILE`

## sort

The sort command outputs the sorted contents of a file. By default, it'll sort the lines alphabetically

Sort file  
`sort FILE`

Sort file in reverse order  
`sort -r FILE`

Sort numbers  
`sort -n FILE`

Ignore duplicates  
`sort -u FILE`

### Sorting by field

We can specify a particular "column" that we want to sort by, using the `-k` option followed by a field number

Example:

```txt
pencil 0.50
flowers 9.99
pie 4.99
soda 0.99
```

`sort -nk2 data.txt`

```txt
pencil 0.50
soda 0.99
pie 4.99
flowers 9.99
```
