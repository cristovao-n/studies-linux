# Environment

### Important

-   understanding environment variables
-   parameter expansion
-   defining aliases

### Useful

-   startup files like `.profile` `.bash_profile` `.bashrc`

### Nice to have

-   customizing the prompt

## Environment

There are environment variables for each shell section

Print the environment  
`printenv`

### Parameter expansion

If we write out the name of an environment variable prefixed with `$`, the shell will replace it with the actual value

`echo $USER`

> Interesting env variables

> `PWD` -> Working directory  
> `OLDPWD` -> Previous working directory

### Defining variables

To define a shell variable, use `key=value`  
Built-in variables are upper-cased, so it's a common convention to lowercase custom variables to prevent confusion  
Shell variables only exist in the current shell instance

`animal=elephant`  
`color="purple"`  
`num=821`

To define an environment variable, use `export key=value`

`export animal=lion`

## Startup files

For non-login sessions (typical session when you launch the terminal)

`etc/bash.bashrc` -> global config for all users  
`~/.bashrc` -> specific settings for each user

## Customizing the prompt

To customize your prompt, edit the PS1 env variable

See `man bash` to learn about reserved characters that provides information like working directory, current time, username, etc

Learn about colors and formatting in bash: [link](https://misc.flogisoft.com/bash/tip_colors_and_formatting)

## Defining Aliases

We can define our own command using the `alias` keyword

`alias ll='ls -al'`

There are a lot of articles online about useful alias
 