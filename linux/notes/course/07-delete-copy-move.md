# Delete, copy and move commands

-   rm command
-   rm -d & rm -r
-   mv command
-   cp command

## rm

Remove a file  
`rm FILE`

Remove an empty directory  
`rm -d DIRECTORY`  
`rmdir DIRECTORY`

Remove directories and their contents recursively  
`rm -r DIRECTORY`

Remove with prompt before every removal  
`rm -ir DIRECTORY`

## mv

Move files to a target directory  
`mv FILE... DIRECTORY`

Move directories to a target directory  
`mv DIRECTORY1... TARGET_DIRECTORY`

Move files and directories to a target directory  
`mv FILE... DIRECTORY... TARGET_DIRECTORY`

### Renaming with mv

Rename a file  
`mv FILE_OLD_NAME FILE_NEW_NAME`

Rename a folder (target folder should not exist)  
`mv FOLDER_OLD_NAME FOLDER_NEW_NAME`

It only works as a renaming tool if we process one file at a time

## cp

Copy file to target directory  
`cp FILE... TARGET_DIRECTORY`

Copy entire directory and give it a new name (target folder should not exist)  
`cp -r FOLDER_OLD_NAME FOLDER_NEW_NAME`

Copy entire directory (target folder should exist)  
`cp -r FOLDER TARGET_DIRECTORY`
