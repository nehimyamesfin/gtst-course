# Linux File Hierarchy
- Linux/Unix have special file systems than windows.
- File system is a directory structure that the OS uses.
## System File
- Are files used by the system software (OS).
> 		==**WINDOWS**== : system files appear under the **local disk C:**
> 		==**Linux**== : system files appear under the **root directory ( / )**.

## File Structure in Detail
### 1. / or (root)
- Every single file and directory starts from the root directory.
- Only **root users has the right to write** under this directory.

### 2. /bin or (binary executables)
- Are **essential command binaries** that need to be available in single-user mode; for all users.
> 		**Example** : cat, ls, cp, pwd …
- **NOT ALL COMMANDS ARE FOUND HERE, LIKE SOME ROOT COMMANDS.**

### 3. /boot or (boot loader files)
- This directory is a **critical component of the root ( / ) filesystem**. **It contains the file needed to successfully start the OS, including the linux kernel, initial RAM disk (initrd) image & bootloader configuration files.**

### 4. /dev or (device directory)
- It **contains device files**, which **represent physical or virtual devices** connected to the system.
- Each device in the system **such as hard drives, network interfaces, USB devices & pseudo-drivers** is represented by a file in the /dev directory.

### 5. /etc or (et cetera)
- It contains **config files required by all programs.**
- This also contains **startup & shutdown shell scripts used to start/stop individuals programs**.

### 6. /home or (home directory)
- Its **home directory for all users** to store their **personal files**.
> 		**Example:** /home/abebe , /home/kebede

### 7. /lib or (libraries)
- This libraries are essential for the binaries in **/bin** & **/sbin**.

### 8. /media
- In this directory **removable media devices like USB drives, CDs & DVDs are automatically mounted when inserted into the system.**
- Its temporary mount directory for removable devices.
> 		**Example:** /media/cdrom ............. for CD-ROM
> 				/media/floppy ............. for floppy

### 9. /mnt or (temporarily mounted files)
- The /mnt directory & sub-directories are **intended for mount points to removable or temporary files storage.** As an example of using mount points, consider plugging a USB flash drive into Linux computer.
- Temporary mounted directory where sysadmins can mount filesystems.

### 10. /opt or (optional application software packages)
- This directory is **reserved for all the software & add-on packages that are not part of the default installation.**
-  Contains add-on applications from individual vendors. Add-on applications should be installed under either **/opt** or **/opt/sub-directory**.
> 		**Example:** Microsoft word, excel.....

### 11. /sbin or (system binaries)
- Just like **/bin** the **/sbin** also **contains binary executables**. The Linux commands located under this directory are **used typically by the system administrator, for system maintenance.**
- Unlike the /bin directory the /sbin directory contains **binary executables & command line tools** that are **preserved for the root user.**
- They **wont run without sudo**.

### 12. /tmp or (temporary files)
- Directory that **contains temporary files created by the system & users**.
- Files under thus directory are **deleted when the system is rebooted or shutdown.**

### 13. /usr or (user utilities)
- This is **one of the most critical directories in the Linux System**. The **/usr** directory is a directory that **comprises libraries, binaries & documentation** for installed software applications.
- System files contained in this directory **are shareable among other users.**

# Text Editors
- Are programs used for text processing.
- Linux command line text editors:
> 	 - VIM*
> 	 - Nano*
> 	 - Emacs
> 	 - Neovim

- Linux Graphical text editors:
	- Sublime
	- VsCode
	- Gedit
	- Pluma .....

#### VIM
- Its a text editor thats **fast & powerful**. 	
> 		==**SYNTAX**==: vim filename

-  It have **mainly two modes**:
> 	- **Command mode ( i )** : where you can do commands.
> 	- **Input mode ( esc )** : where you can write your inputs.

- Some commands:
> 	- **SAVE** ==:w + enter==
> 	- **QUITE** ==:q + enter==
> 	- **FORCE QUITE & SAVE** ==:wq! + enter==
> 	- **UNDO** ==:u==
> 	- **Execute bash commands** ==:%!yourcommand== ..... there is no space between them.

#### Nano
- Its a **user-friendly, free & open-source** text editor.
> 		**SYNTAX**: nano filename

- Some shortcuts:
> 	1. ==SAVE==    - **ctrl + s**
> 	2. ==UNDO==  - **alt + u**
> 	3. ==REDO==   - **alt + e**
> 	4. ==EXIT==     - **ctrl + x**
> 	5. ==COPY==   - **ctrl + shift + c**
> 	6. ==CUT==     - **ctrl + shift + x**
> 	7. ==PASTE==  - **ctrl + shift + v** 


# Linux User Management
- On Linux there is **two kinds of users**:
	- **ROOT**, **id=0**
	- **Normal User**, **id=1-999**
## Creating Users
- On linux to create users you can use the following commands:
		==**SYNTAX**==: sudo **useradd** username ........... simple
			   sudo **adduser** username ......... detailed

- **When you create a user it creates a group with that name.**
- The **user files** are stored inside **/etc/passwd**.
- The **user password** are stored inside **/etc/shadow**.


#BE_HARD_WORKER
#YOU_CAN_DO_IT