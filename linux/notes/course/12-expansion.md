# Expansion

### Important

-   pathname expansion
-   brace expansion
-   quoting

### Useful

-   command substitution

### Nice to have

-   arithmetic expansion
-   tilde expansion

## Pathname expansion

We can use special wildcards characters to build patterns that can match multiple filenames at once  
The shell will expand all files that matches the pattern  
Then the files are passed as arguments to the command

### \* wildcard

The asterisk `*` character represents zero or more characters

List all files ending with `.txt`  
`ls -l *.txt` --> `ls -l data.txt greeting.txt phones.txt pho.txt`

Combine all files ending with `.txt`  
`cat *.txt`

### ? wildcard

The question mark `?` character represents any single character

Match any files named `app` that end with two character file extensions like `app.js` or `app.py` but not `app.css`  
`ls app.??`

Match files like `pic1.png`, `pic2.png`  
`ls pic?.png`

### Range wildcards

Inside of square brackets `[]` we can specify a range of characters to match

Match `pic1.png`, `pic2.png`, `pic3.png`  
`ls pic[123].png`

Match `file1`, `file2`, `file3`, up to `file9`  
`ls file[0-9].png`

Match any files that begin with a capital `A, B, C, D, E, or F`  
`ls [A-F]*`

#### Negating Ranges

Inside of square brackets `[]` we can specify a range of characters to **not** match, using a caret `^`

Match any files that don't start with `a`  
`ls [^a]*`

Match any files that don't start with a numeric digit  
`ls [^0-9]*`

## Tilde expansion

`~` is expanded to the logged in user's home directory  
It's expanded before the command is actually run  
`echo ~` --> `/home/cristovao`

## Brace expansion

Brace expansion is used to generate **arbitrary strings**  
The specified strings inside of curly braces `{}` are used to generate all possible combinations with the optional prefixes and suffixes

Generate three new files: `page1.txt`, `page2.txt` and `page3.txt`  
`touch page{1,2,3}.txt`

Print weekdays planners in stdout  
`echo {mon,tue,wed,thu,fri}-{am,pm}-planner.txt`

### Ranges

`echo jan{1..31}` --> `jan1 jan2 jan3 ... jan31`  
`echo {2..10..2}` --> `2 4 6 8 10`  
`echo group-{a..e}` --> `group-a group-b group-c group-d group-e`

Create directories  
`mkdir -p {mon,tue,wed,thu,fri,sat,sun}/{breakfast,lunch,dinner}`

### Nested brace expansion

`echo {x,y{1..5},z}` --> `x y1 y2 y3 y4 y5 z`

## Arithmetic expansion

The shell will perform arithmetic via expansion using the `$((EXPRESSION))` syntax

`echo $((10+3))`  
`echo $((10%3))`

## Quoting

`echo look at          me` --> `look at me`  
`echo holy $hit` --> `holy`

### Double quotes

If we wrap text in double quotes, the shell will respect our spacing and will ignore special characters except for: **$ \ `**  
Pathname expansion, brace expansion and word splitting will be ignored

### Single quotes

Use single quotes to suppress all forms of substitution  
`echo "$((2+2)) is 4"` --> `4 is 4`  
`echo '$((2+2)) is 4'` --> `$((2+2)) is 4`

## Command substitution

We can use the `$(COMMAND)` syntax to display the output of another command

`echo "today is $(date)`  
`echo Hello there $(whoami)`
