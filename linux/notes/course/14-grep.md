# Grep

### Important

-   grep basics
-   common grep options

### Useful

-   extended regex syntax

## Recursive search

Use `-r` option to search for all files under a directory

Usage:  
`grep -r "pattern"`

## Grep options

Match only entire words  
`grep -w "pattern" file`

Count number of matches  
`grep -c "pattern" file`

Show context of the match, lines after and before  
`grep -A2 -B2 "pattern" file`  
`grep -C2 "pattern" file`

Show line number of the match  
`grep -n "pattern" file`

## Using regex in Grep

Grep supports regular expressions, just pass the regex as a pattern and use the `E` option

`grep -E "regex" file`

## Piping to grep

A common use case is to use `grep` to whittle down or filter a large chunk of data

Get all processes running in the machine and filter to only the processes that include "discord"  
`ps -aux | grep discord`

## Finding file paths by content

Show the file name, not the result itself  
`grep -l "pattern" file`
