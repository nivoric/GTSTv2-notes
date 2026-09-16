## Linux User Management
- On computer system, person who uses the computer is called ==user==.
- Every users have group, **users have their own files and applications**.
- To know your name in linux -> `whoami`.
- Those users have power/privilege, On Linux there are 2 kind of users:
	- Root id = 0
	- Normal user id = 1-999
- The root user have the power to do everything on linux, but if users want to have a root access they add ==sudo== in front of the command.
![[sudo_and_user_diff.png]]
- **sudo** = superuser do, used to pass "permission denied" or failure when downloading packages without using the **sudo** command.
### Creating users
- On linux, to create users you can use the following commands.
	- `Useradd` -> simple one
	- `Adduser` -> detailed
- Useradd command = `sudo useradd new_username`.
- Adduser command = `sudo adduser new_username`.
- User files are stored in /etc/passwd
- The passwords are stored inside /etc/shadow
- When you create a user ==it creates a group with that name==.
### To access root user
- `sudo su`
### Other advanced user commands
- To change password of user = `sudo passwd username`
- To change user id = `sudo usermod -u new_id username`
- To delete user = `sudo userdel -r username`
- To change users while being in terminal = `su - username`
- `sudo mkhomedir_helper <your username>`:
    - is used to create a home directory for a specified user in Linux, typically when the user is being added to the system without an existing home directory.
- `sudo usermod <your username> -s /bin/<shell>`:
    - changes the default login shell for the specified user to the specified shell (e.g. /bin/bash, /bin/zsh)
- Create a new group (if not already created) = `sudo groupadd <group_name>`.
- Add user to the group = `sudo usermod -aG <group_name><username>`.
- Verify the user's group membership = `groups <username>`.
- Remove user from the group = `sudo gpasswd -d <username> <group_name>`.
- Verify the user's group membership = `groups <username>`.
## Sudoers file 
- The **sudoers** file is a file Linux and Unix administration use to allocate system rights to system users.
- The user you created doesn't have power to use ==sudo== as the original one.
- This is because it is not added in the sudoers file.
- To access this file:
```bash
sudo visudo
```
- You can add the user, you need to have access to the sudoers file, so he can use the sudo command.
- Then after the user can use sudo command.
## Linux file permission
- Every file on linux have their own = **owner and permission**.
- There is 5 main parts on the listing = **Permission, Owners, Date, Size, file name**.
### Ownership
- Ownership the owner of the file
- This has 2 kinds = **User and Group**.
- To change the owner of file you can use the command:
```bash
sudo chown user:group filename
```
### Permission
- There are 3 types of permissions:
	- Read (r)
	- Write (w)
	- Execute (x)
- The folders and files are different with the 'd' and the '-' on the beginning of the permission. Files start with '-' and folders start with 'd'.
- Permission has 3 parts = **user-group-other**.
- user (u) = power of user defined on the ownership
- group (g) = power of group defined on the ownership
- Other (o) = power of other users outside of the group.
- To change permission of file
```bash
sudo chmod <option> filename
```
#### chmod permission
- This command helps to change file permission
- Those file permissions are **read, write and execute**.
- Each of the permissions have a number representations:
	- Read -> 4 - r
	- Write -> 2 - w
	- Execute -> 1 - x
- The parameter can be in numbers and symbols
**A. Parameters in symbol**:
	- `chmod a+x file_name` = adding execute permission for all (`chmod +x filename`).
	- `chmod u+x file_name` = adding executing permission for user.
	- `chmod g+x file_name` = adding execute permission for group.
	- `chmod o+x file_name` = adding executing permission for other users.
	- `chmod -x file_name` = removing execute permission for all.
	- `chmod a+rwx, u-rw, g-x, o-xw file_name` = gives rwx for all and removes something from all.
**B. Parameters in Number**:
	- `chmod 621 file_name` = 6(rw) for user, 2(w) for group, 1(x) for other.
	- `chmod 777 file_name` = 7(rwx) for users, 7(rwx) for group, 7(rwx) for others.
### Special file permissions
- There are another 3 special permissions, you may encounter on your pentesting journey.
- They are:
	- `SUID bits(s)` - set user ID bit - add 4 infront of our numeric value - 4000
	- `SGID bits(s)` - set group ID bit - add 2 infront our numeric value - 2777
	- `Sticky bits(t)` - set other ID bit - add 1 infront of our numeric value -> 1602
- These are permissions like the execute (x), but they will set the execute permission to the user who settled them.
- Example: if Mr. a add SUID bit to a program then any user can execute the program with permission of Mr. a
## Package installation on linux
- On linux, to install software, you use package managers. E.g. **apt, pacman, pkg**.
- We will use debian package manager and it is called "**APT**" and there is also "**dpkg**".
- Package managers are a free-software user interface that work with an online server to handle the installation and removal of software on debian and debian-based linux distributions.
- Common apt commands:
```bash
sudo apt update = to update packages on Linux
sudo apt search <software_name> = to search for packages on Linux
sudo apt install <software_name> = to install packages on linux
sudo apt upgrade = to upgrade packages on linux
sudo apt purge <software_name>
```
### Package dependencies
- A software can be built based on another program called '==modules=='. so, for a program to work properly, the dependencies have to be installed successfully.
- Those package managers install the software + dependencies.
## Common Linux Repository Errors
1. **Could not get lock/var/lib/apt/lists/lock:** This occurs when you run 2 different apt's or if there is another apt process running on background, for this you can simply solve it by restarting your PCs or closing the another apt processes.
2. **Could not open lock/var/lib/dpkg/lock-front-end:** This occurs when you forget to run apt with root user aka 'sudo'
3. **Unable to locate package**: This occurs when you misspell the program's name. 
4. **The repository 'https://kali.org/kali kali-rolling Release' doesn't have a release file** = This occurs when there is a problem on the repository configuration. Sometimes the link might be broken. You have to put the correct link 'deb https://http.kali.org/kali kali-rolling main contrib non-free'. this might differ based on the distro so you can search the repository link on google or ChatGPT.
### Some cautions
- Don't close apt while installing something
- If repository error happens, you can fix it using = `sudo apt edit-sources`.
- For those kinds of errors what you have to do is google/youtube {detail we will see this while we learn footprinting}.
### Dpkg / Debian Package Manager /
- Dpkg is an offline package managing program. Packages on debian have an extensions ".deb"
- Syntax:
```bash
sudo dpkg -i <package_name> = installs the package into the system
sudo dpkg -r <package_name> = removes the package from the system
sudo dpkg -p <package_name> = purges an installed or already removed package from the sysem
```
