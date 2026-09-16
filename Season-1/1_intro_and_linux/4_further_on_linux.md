## Linux file hierarchy
- Linux/UNIX have a special file system than windows. File system is a directory structure that the OS uses.

## System files
- System files are files used by the system software (OS).
- **Windows** = system files appear under the local disk (C:).
- **Linux** = system files appear under the root directory ( / )

### System files in Linux
**1. Root ( / )**: 
- every single file and directory starts from the root directory. The only root user has the right to write under this directory.
- /root is the root user's home directory, which is not the same as /.

**2. bin - Binary executables**:
- Essential command binaries that need to be available in single-user mode; for all users.
- E.g. = cat, ls, cp, pwd.
![[bin_folder.png]]

**3. /boot - Boot loader files**:
- Kernel initrd, vmlinux, grub files are located under /boot.
- Example:
	- initrd.img-2.6.32-24-generic, vmlinuz-2.6.32-24-generic.
![[boot_folder.png]]

**4. /dev - Essential device files**:
- These include terminal devices, usb, or any device attached to the system.
- Example: /dev/tty1, /dev/usbmon0
![[dev_folder.png]]

**5. /etc - etc cetera**:
- Contains configuration files required by all programs. This also contains startup and shutdown shell scripts used to start/stop individual programs.
- Example: /etc/resolv.conf, /etc/hosts.
![[etc_folders.png]]

**6. /home - Home directory**:
- Home directories for all users to store their personal files.
- Here, you can't access files of other users.
- Example = if your home is /home/nathan, you can't access /home/rexder. Your home directory by "~".

**7. /lib - Libraries essential for the binaries in /bin & /sbin**:
- Library filenames are either ld* or lib*.so*
- Example = ld-2.11.1.so, libncurses.so.5.7
![[lib_folder.png]]

**8. /media - Media points for removable media such as CD-ROMs**:
- Temporary mount directory for removable devices.
- Examples: /media/cdrom for CD-ROM; /media/floppy for floppy drives; /media/cd recorder for CD Writer.

**9. /mnt - temporarily mounted files**:
- Temporary mount directory where sysadmins can mount filesystems.

**10. /opt - optional application software packages**:
- Contains add-on applications from individual vendors.
- Add-on applications should be under either /opt/ or /opt/sub-directory.
![[media_folder.png]]

**11. /sbin - essential system binaries**:
- Just like /bin, /sbin also contains binary executables. The linux commands located under this directory are used typically by system administrator, for system maintenance purposes.
![[sbin_folder.png]]

**12. /tmp - Temporary files**:
- Directory that contains temporary files created by system and users. Files under this directory are deleted when system is rebooted.
![[tmp_folder.png]]

## Text editors
- Programs that are used for text processing
- Linux command line text editors:
	- VIM
	- Nano
	- Emacs
	- Neovim
- Linux graphical text editors:
	- Sublime
	- VScode
	- Gedit
	- Pluma

### VIM - Vi Improved
- Before, vi was the primary editor used on Unix, the **Line editor** was used. User was able to see/edit only one line of the text at a time.
- Then the vi-editor improved and developed VIM. it is:
	- a very powerful editor,
	- but at the same time, it is cryptic and
	- it is hard to learn, specifically for windows users.
- Syntax = `vim 'yourfilename'`. 
- It have mainly 4 modes:
	- Command mode = to enter this mode, just press the "Esc" button to switch into normal mode   and then to use commands you can just type them like this:
        - `Normal mode -> :%your_command` = some commands don't need the "%" sign.
        - To save = `:w` and to exit `:q`. To force the save/exit, just add "!" at the end.
	- Input mode = to enter this mode, just press I.
	- Visual mode = to enter this mode just press V
	- Normal mode = to enter this mode, just press "Esc" button.
![[vim-page.png]]

### Nano
- The GNU Nano text editor is a user-friendly, free and open-source text editor that usually comes pre-installed in modern Linux systems.

#### Nano hotkeys
- `nano file_name` = to enter your file in nano
- Ctrl + S = save the file
- Alt + U = Undo
- Alt + E = Redo
- Ctrl + X = Exit
- Ctrl + Shift + C = Copy
- Ctrl + Shift + X = Cut
- Ctrl + Shift + V = Paste
