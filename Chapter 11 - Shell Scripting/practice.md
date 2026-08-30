### Task :
Create 3 sam folders Each folder contains 10 files In the last third file we need to enter text.
### Solution :

- Created loopTask.sh
```bash
vim loopTask.sh
```
- Inside the loopTask.sh
```bash
#! /usr/bin/bash
#Create 3 sam folders
#Each folder contains 10 files
#In the last third file we need to enter text

num=3
index=1

while [ $index  -le $num ]
do
        mkdir sam$index
        echo "sam$index folder Created Successfully"

        for((i = 1; i <= 10; i++))
        do
                touch sam$index/file$i
                echo "file$i Created Successfully"
                if [ $index -eq 3 ] && [ $i -eq 3 ]
                then
                        echo "This text is from sam3 file3" >> sam$index/file$i
                fi
        done

        ((index++))
done

cat sam3/file3
```
- Then run the script 
```bash
./loopTask.sh
```
- output :
```bash
sam1 folder Created Successfully
file1 Created Successfully
file2 Created Successfully
file3 Created Successfully
file4 Created Successfully
file5 Created Successfully
file6 Created Successfully
file7 Created Successfully
file8 Created Successfully
file9 Created Successfully
file10 Created Successfully
sam2 folder Created Successfully
file1 Created Successfully
file2 Created Successfully
file3 Created Successfully
file4 Created Successfully
file5 Created Successfully
file6 Created Successfully
file7 Created Successfully
file8 Created Successfully
file9 Created Successfully
file10 Created Successfully
sam3 folder Created Successfully
file1 Created Successfully
file2 Created Successfully
file3 Created Successfully
file4 Created Successfully
file5 Created Successfully
file6 Created Successfully
file7 Created Successfully
file8 Created Successfully
file9 Created Successfully
file10 Created Successfully
This text is from sam3 file3
```