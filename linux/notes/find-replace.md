# Find & Replace

## sed

> You can use any character as the delimiter, the most common is /

### Using literal strings

Replace all occurrences of find to replace and prints the result in the standard output  
`sed 's/find/replace/g' file.txt`

Replace all occurrences of find to replace in the file itself, in place  
`sed -i 's/find/replace/g' file.txt`

You can pass more than one file  
`sed -i 's/find/replace/g' *.txt`

If you need to apply sed in a directory recursively, use it with find command  
`find /path -type f -exec sed -i 's/find/replace/g' '{}' ';'`

> Use grep if you need more performance or less side effects
> https://stackoverflow.com/questions/6178498/using-grep-and-sed-to-find-and-replace-a-string

### Using regex

Replace a single-line text  
`sed s/(regex-group)/\1/g file.txt`

## tr

The `tr` command is designed for single-character manipulation

Convert all letters to uppercase  
`echo "Hello World" | tr [a-z] [A-Z]`

Remove lowercase characters from input  
`echo "Hello World" | tr -d [a-z]`

Remove duplicated "t" characters  
`cat usernames.txt | tr -s "t"`

Remove duplicated " " characters  
`"echo "This   is a   text" | tr -d " "`

Replace a character  
`cat message.txt | tr "!" "."`

Replace a multi-line text  
``

> More about **tr** and **sed**:
>
> [How can I replace each newline (\n) with a space using sed?](https://stackoverflow.com/questions/1251999/how-can-i-replace-each-newline-n-with-a-space-using-sed)
