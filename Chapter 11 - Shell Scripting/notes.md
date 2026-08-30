### Shell Scripting
- Shell scripting is basically the process of writing commands in file and Linux will excecute them automatically.
- Linux command + Logic + Automation = Shell Script.
- common shells 
    - Bash (IMP)
    - sh
    - zsh
    - fish
- A shell is a program that allows you to communicate with Linux

### shebang :
- It tells to Linux that use Bash to excecute this particular script.
```bash
#!/usr/bin/bash
```

### Varibles :
- Variables are like containers that stores values.
   - System Variables
   - Userdefined Variables
    #### 1. System Variables :
    - These are generally predefined shell / environment varibles supplied by the system or shell.
    - Ex :
    ```bash
    echo "$USER"
    echo "$HOME"
    echo "$PWD"
    ```
    #### 2. Userdefined Variables :
    - These are created by user.
    - Ex :
     ```bash
    name="Rohit"
    ```

### User Input :
- To take user input you should use **`read`**
- Ex :
    ```bash
    echo "Enter your name"
    read name
    echo $name
    ```
- Arguments 
    - **`-p`** : Input takes in same line
    - **`-s`** : Input is invisible while typing

### Conditional Statements :
- **`-gt`** : Greater than (>)
- **`-lt`** : Less than (<)
- **`-eq`** : Equals to (=)
- **`-ne`** : Not Equals to (!=)
- **`-ge`** : Greater than or Equals to (>=)
- **`-le`** : Less than or Equals to (<=)

```bash
if [ "$age" -gt 18 ] 
then
    echo "Eligible"
else
    echo "Not eligible"
fi
```

### Loops :
- If you know the range then you can use it
```bash
for i in {1..10}
do
    echo "$i"
done
```
- If you are taking the range from variable then you should use this and you dont need to use **`$`** when you are using the variable inside **`(( ))`**.

```bash
num=10

for((i = 1; i <= num; i++))
do
    echo "$i"
done
```
- While loop
```bash
while [ "$num" -gt 0 ]
do
    echo "$num"
    ((num--))
done
```