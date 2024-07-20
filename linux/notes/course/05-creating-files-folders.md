# Creating Files and Folders

-   touch command
-   mkdir command
-   file command
-   File naming tips

## touch

The `touch` command was originally created to update the modification date of an existing file  
However, it creates a new file if the provided file does not exists, and that's how it's is widely used by the users

## file

There's a difference between the extension and the actual file type  
The file extension is not what decides the file type

Example:  
We can remove the `.png` extension of a PNG file, and it's type will still be PNG

```sh
file image.png
# PNG image data
mv image.png image
file image
# PNG image data
mv image image.txt
file image
# PNG image data
```

However, the OS will use the file extension to decide what application will be used to open the file  
Extensions do matter, they will be used by the OS to open the file with the right application, but they don't determine the actual file type

## mkdir

Create parent directories if they don't exist  
`mkdir -p a/b/c/d/e`
