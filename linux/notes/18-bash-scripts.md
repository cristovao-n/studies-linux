# Bash scripts

## Writing our first script

### Shebang

The first line of a bash script is called the "shebang"  
It's used to tell the OS which interpreter it should use when parsing the file

`#!/bin/bash`

### Comments

Comments starts with `#`

### PATH variable

The `PATH` variable contains a list of directories that shell will look for executable programs  

Commands that require sudo privileges are usually stored in `sbin` directories

#### Adding custom scripts per user basis

Add a directory called `bin` in the home directory  
`mkdir ~/bin`

Move the script  
`mv script bin/`

Add the directory to the PATH variable if it's not there  
.bashrc  
`PATH="$HOME/bin:$PATH"`

Make the script executable  
`chmod +x script`

