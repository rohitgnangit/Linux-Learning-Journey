### `cd` : 
- It will take you to home directory
---
### `ls` :
- **It shows the list of file in current folder**
---
### `ls > /dev/null` :
- This redirects STDOUT to the null device, so you cant see output on screen
---
### `ls ilwehgi > /dev/null` :
- This command shows that "no such directory" msg on screen
---
### `ls ilwehgi 2> /dev/null` :
- Now you will no longer see the error
---
### `ls ilwehgi /etc 2> /dev/null` :
- This shows the contents of the /etc folder while hiding the error msg
---
### `ls ilwehgi /etc 2> /dev/null > output` :
- In this command, you still write the error message to /dev/null while sending STDOUT to a file with the name output that will be created in your home directory
---
### `cat output` :
- to show the contents of this file
---
### `echo hello > output` :
- This overwrites the contents of the output file. Verify this by using cat output again
---
### `ls >> output` :
- This appends the result of the ls command to the output file. Type cat output to verify
---
### `ls -R /.` :
- This shows a long list of files and folders scrolling over your computer monitor. (You might want to press Ctrl-C to stop [or wait some time])
---
### `ls -R /. | less` : 
- This shows the same result, but in the less pager, where you can scroll up and down using the arrow keys on your keyboard Type q to close less
---
###  `ls > /dev/tty1` :
- This gives an error message because you are executing the command as an ordinary user, and ordinary users cannot address device files directly (unless you were logged in to tty1). Only the user root has permission to write to device files directly