## Wild Card :
- In Linux wild card is a special character thats let you match files / directoris based on a pattern.
- Instaed of typing every filename individually you can use wild cards.
    - #### **`*`**
    - #### **`?`**
    - #### **`[]`**

#### 1. **`*`** :
- Suppose we have 
    - f1.txt
    - f2.txt
    - f3.txt
    - photo.jpg
- Run 
```bash
ls *.txt
o/p : It list all files match with .txt
      f1.txt
      f2.txt
      f3.txt
```
#### 2. **`?`** :
- it represents exactly on character
- Ex :
```bash
ls file?.txt
o/p : file1.txt -> file9.txt
```
#### 3. **`[]`** :
- It matches one character from set
- Ex :
```bash
ls file[123].txt
o/p : file1.txt
      file2.txt
      file3.txt
```
- we can also specify a range
- Ex :
```bash
ls file[1-5].txt
```
## Redirection :
- **`>`**
- **`>>`**

1. **`>`** :
- It sends the command output into file
- Ex :
```bash
echo "Hello" > file.txt
```
- If file.txt doesn't exist then it creates it
- If file.txt already exist the it overwrites the existing content

2. **`>>`** :
- It also sends output to file but adds it to end instaed of overwrite
- Ex :
```bash
echo "cloud" >> file.txt
```

## Pipe (|) :
- we can execute two or more commands at a time
- Ex :
```bash
cat file.txt | sort
```
- The first command output will goes input for second command

## grep :
- It is used to search for text or pattern inside files or command output.
- Ex :
```bash
grep "Linux" file.txt
o/p : It will highlight the "Linux" word in file.txt
```
- `-i` for case insensitive
- `-n` to get line numbers



