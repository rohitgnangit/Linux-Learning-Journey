### `vim` :
This command is used to create and edit the file, `vim` is advanced version of `vi` command. It gives more features that `vi`. 

-  **`i`** : To insert the content in the file.
- **`esc`** : Escape from insert mode.
- **`:wq`** : Save and exit from file.
- **`:q!`** : Quit from file without saving any changes.
- **`w`** : Saving the file.
- **`q`** : Just quit from file.
- **`u`** : undo, it will get you back one step.
- **`gg`** : Goes to the first in file.
- **`G`** : Goes to the end of the file.
- **`/text`** : Searches for the text forward from current cursor point.
""**note** : *You should mention the word at the pplace of text which you want to search"* .
- **`?text`** : Searches for the text backward from current cursor point.
- **`:%s/old/new/g`** : This command is usefull to change all old occurences with new one.
"**note**: *You should mention current occurrence in the place of "old" and new occurrence in the place of "new"*".
---
### `echo` :
- Used to display the value of variable.
```bash
Ex : 'echo $PATH'
o/p : It displays the value of path environment variables.
```
---
### `man` :
- Used to know information about the command.

```bash
Ex : 'man vim'
o/p : It shows entire information about vim command like what is the use of it and how many internal commands there.
```

### `man -k` :
- Used to know the commands related to particular work
```bash
Ex : 'man -k edit'
o/p : It shows the all commands related to edit work.
```