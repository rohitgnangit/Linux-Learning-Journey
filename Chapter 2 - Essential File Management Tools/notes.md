### Directories :
- `/` : Root of the file system and everything starts from here.
- `/home` : Home directory of normal users, our personnel files are here.
- `/root` : Home directory of the root users.
- `/etc` : System configuration files.
- `/var` : Variable data (logs, mail, cache).
- `/tmp` : Temporary files, files may be deleted after reboot.
- `/usr` : User programs, libraries, documentation and most installed features end here.
- `/boot` : Kernal and bootloader files, requires to boot Linux.
- `/dev` : Device files. Represents disks, terminals, USB devices etc.
- `/proc` : Process and kernal information, Virtual filesystem with system info.
- `/sys` : Hardware and kernal interface Used to view/manage hardware through the kernel.
- `/media` : Automatically mounted removable devices, USB drives, CDs, DVDs.
- `/mnt` : Temporary manual mount point, Used when you manually mount a filesystem.

### Mounting :
Mounting is the process of connection between device and directory.

Ex : Suppose we have a USB. To access the files from USB we need to mount it
```bash
sudo mount /dev/sbd1 /mnt
```
This means :
- `/dev/sbd1` - the disk/partition
- `/mnt` - the directory where you access its files

After mounting we can use :
```bash
cd /mnt
ls
```
### Absolute Pathname :
- An absolute pathname always starts from the root directory '/'
- We can access any file from any folder using this method.

### Relative Pathname :
- An relative pathname starts from current working directory '/home/rohit'.
- We can access the files only consists in this directory.

### Link :
A link is simply a another way of accessing file or directory.
- #### Hard Link :
  - Another name for the same file, if you delete one the other one remains.
  
  Ex : 
  ```bash
  ln file1 file2
  ```

- #### Symbolic (Soft) Link :
    - Like the windows shortcut, if the original will deleted then shortcut stop working.
    
    Ex :
    ```bash
    ln -s file1 shortcut
    ```
- #### inodes :
  - An inode is a internal data structure Linux uses to stores information about files. 
