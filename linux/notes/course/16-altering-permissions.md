# Permissions basics

### Important

-   chmod command basics
-   sudo command

### Useful

-   chown command

### Nice to have

-   chmod octal notation
-   su command
-   working with groups: addgroup, adduser

## chmod (change mode)

chmod command is used to change the permissions of a file or directory

To use it, we need to tell it:

-   who we are changing permissions for
-   what change are we making
-   which permissions are we setting

`u` owner of the file
`g` group owner
`o` others
`a` all of the above

Add write permissions to the group  
`chmod g+w file.txt`

Remove write permissions from all  
`chmod a-w file.txt`

Add executable permissions for owner  
`chmod u+x file.txt`

Set permissions to read ONLY for all  
`chmod a=r file.txt`

### octal notation

We can use an octal number to represent the combination of permissions for the three permission groups

Example:  
`chmod 755 file.txt` -> `111 101 101` -> `-rwx r-x r-x`
`chmod 644 file.txt` -> `110 100 100` -> `-rw- r-- r--`

## su (substitute user)

There may be times we want to start a shell as another user, from within our own shell session

Create a new login shell for the user hermione  
`su - hermione`

Leave session  
`exit`

## Root user

In Linux systems, there is a super user called root. The root user can run any command and access any file on the machine, regardless of the file's actual owner

The root user has tons of power and could easily damage or even destroy the system by running the wrong commands

For this reason, ubuntu locks the root user by default and we don't know it's password

### sudo (super user do)

Even if the root user is locked by default, we can still run specific commands as the root user by using the `sudo` command

The first created user in the OS and the users created as administrators are allowed to run all commands using `sudo` and entering the password of the user

See the allowed commands for the current user  
`sudo -l`

By default, the password is cached on a per-terminal basis for 15 minutes

### Editing sudo PATH

The PATH environment variable for the root user differs from the PATH for regular users.

Edit root PATH  
`sudo visudo`

## chown

The `chown` command is used to change the owner and/or the group owner of a specific file or directory

Make bojack the owner of file.txt  
`chown bojack file.txt`

Change the file group owner  
`chown :horses file.txt`

Change both file owner and group owner  
`chown bojack:horses file.txt`

usermod... ?
