**`less`** : Opens the text file in reader which allows easy read.

**`cat`** : Shows the content of the text file on the screen.

**`head`** : Shows the top of the text file.
- `head -n 5 /etc/passwd` : Shows top five lines.

**`tail`** : Shows the bottom of the text file.
- `tail -n 5 /etc/passwd` : Shows bottom five lines.

**`cut`** : Used to quit often when working with Linux files.
- `cut -d ":" -f 1 /etc/passwd` : Extracts only user names

**`sort`** : Display the content in alphabetical order.
- `sort -r file` : Reverse order.
- `sort -n file` : Sort numbers numerically.
- `sort -k 2 file` : Sort using secont field or column.