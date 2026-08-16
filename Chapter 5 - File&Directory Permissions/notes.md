## Files & Directory Permissions :
- If we use **`ls -l`** then we can get files list incluiding permissions
- In that list,

    **`-`** : Represents file

    **`d`** : Represents directory

    **`r`** : Represents Read -> **`4`**

    **`w`** : Represents Write -> **`2`**

    **`x`** : Represents Execute -> **`1`**
- rw-rw-r-- rohit rohit 12 aug 10 13:59

### Change Permissions :
1. chmod
2. chown

- If we need to add any permission then we should use **`+`**

Ex :
```bash
chmod +x file.txt
```
- For delete permission use **`-`**

Ex :
```bash
chmod -x file.txt
```
- We can also specify the permissions by using numbers 

Ex :
```bash
chmod 143 file.txt
o/p : - --xr---wx
```