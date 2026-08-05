### `ls` :
Shows list of files.
- **`ls -l`** : Shows files in long format with detailed information.
- **`ls -a`** : Shows all files including hidden files.
- **`ls -la`** : Combines `-l` and `-a` to show a detailed listing of all files including hidden ones.
- **`ls -lh`** : Displays file size in human-readable format (KB, MB, GB).
- **`ls -lt`** : Sorts files by modification time (newest first).
- **`ls -lrt`** : Sorts files by modification time with oldest first and newest last. Very useful for checking recently modified files.
- **`ls -R`** : Recursively lists all files and subdirectories.

### `cp`: 
Copy the files.
- **`cp file1.txt file2.txt`** : Copies entire file1 to file2.
- **`cp -R source destination`** : Copies directory and all its files and subdirectory recursively.
- **`cp -a source destination`** : Copies files or directories in archive mode, preserving permissions, ownership, timestamps, symbolic links, and other file attributes.

### `mv` :
To move file to a particular directory.

```bash
Ex : mv filename /directory
```

### `rm` :
To remove or delete the file.
- **`rm file`** : Delete the file.
- **`rm -r directory`** : Delete the directory.
- **`rm -f file`** : Forces deletion without asking for confirmation.
- **`rm -rf directory`** : Forcefully deletes a directory and all its contents recursively.

### `ln` :
This command is used to link two files.
Ex :
```bash
# 1. Hard Link
ln file1 file2        //the file2 is same as file1 because both are linked if file1 deletes file2 exist.
# 2. Soft Link
ln -s file1 shortcut  // shortcut is the shortcut of file1 we can access the file1 with shortcut.
```

### `tar` :
**`tar`** is used to archive multiple files and directories into a single file.
By itself **`tar`** does not compress files.
Compression can be added using options like **`-z`**(gzip).

#### Syntax :
```bash
tar [options] archive_name files/directories
```

#### Option : Meaning
- **`c`** : Create a new archive
- **`v`** :	Verbose (show progress)
- **`f`** : Specify archive filename
- **`t`** : List archive contents
- **`x`** : Extract archive
- **`z`** :	Compress/Decompress using gzip (.tar.gz)
