## History of Linux
- Linux is a kernel, not an operating system like most people think.
- A **kernel** is a code/program that is used to meet your software and hardware (works like a connector between the both) and also allocate resources.
- In 1969 a team led by computer scientists **Ken Thompson and Dennis Ritchie** created the first version of UNIX on a P**DP-7 minicomputer** which was chosen mainly because of Thompson's familiarity with the system from his hobby work on it.
- *BUT IT WASN'T CHEAP AND IT WASN'T OPEN SOURCE!*
- Then a person called "Linus Torvalds" created the Linux kernel and posted it online to make it open source and it was developed n the "C programming language". You can find the source code of the Linux kernel on his GitHub page

## Continuation
- **Richard Stallman** announced the GNU project in 1983 and co-founded the Free software foundation in 1985.
- GNU is a free software replacement to the UNIX OS. But it was just software replacement, not a full OS.
- **So GNU + Linux will give the GNU/Linux OS**. The GNU project was started to create a UNIX-Like operating system created with source code that could be copied, modified and redistributed.
## What is a shell?
- Users communicate with the kernel by the *shell*.
- The shell is a command line interpreter (aka **CLI**). It translates commands entered by the user and converts them into a language that is understood by the Kernel.
- Based on their features and looks there are many shells like:
	- SH
	- BASH
	- ZSH
	- FISH
- They differ in coloring, piping, command compilation and some kind of features.
- To identify your shell:
```
echo $SHELL
```
## What is an Operating system?
- Operating system or OS = the main software part of the computer or basically the soul of the computer.
- It contains:
	- Kernel
	- Softwares
	- Desktop Environments (DEs) = are graphical interfaces that provides users with a visual way to interact with the GNU/Linux Operating System.
	- File extensions
	- Windows manager = This includes **i3, Hyprland, sway, dwm** and much more. Window managers make your setup more productive and also more keyboard-centric, which maximizes productivity specially for coders and people in tech.
- **When it comes to the question of "which desktop environment is the best", the answer depends on:-**
	- Speed, which can be affected by:
		- Animations
		- High graphics and
		- Quality
	- Do you have a high-end PC or a low-end PC? (this is a question to answer first!)
## Why use Linux?
- Linux is fast = You don't need a high spec/high-end computer to run Linux unlike windows.
- 47% of professional developers use Linux-based operating systems
- Linux powers 39.2% of websites whose operating system is known
- Linux powers 85% of smartphones (Hayden James)
- Linux is the third most popular desktop OS, has a market share of 2.09%.
- The Linux market size worldwide will reach $15.64 billion by 2027.
- The world's top 500 fastest supercomputers all run on Linux
- 96.3% of the top one million web servers are running Linux
- Today, there are over 600 active Linux distros
- Most hacking run on Linux
- Linux is the most secured OS.
## Linux Distributions/Distros
- A distro is a modified Linux kernel, type of operating systems with different:
	- Linux Kernel
	- Packages (GNU)
	- Package manager
	- Desktop User Interface.
- Most Linux distros are based on:
	- Debian (Ubuntu, Kali Linux and Parrot are main examples) and
	- Arch (Black arch, Garuda, Fedora and Manjaro are main examples)
## Do windows have distros?
- Windows is not an open source operating system, so it doesn't have any other kind of its own. It just give update and adds some features on it.
## How can we use Linux on our machine?
1. **Main boot** = as a main OS on your machine
2. **Dual boot** = alongside your main OS by partitioning your hard disk/solid state drive
3. **Live Boot** = Use Linux on a usb drive/hard disk with or without persistence
4. **Cloud Terminals** = For old PCs or Low-end PCs, you can use terminals on the web using cloud terminals.
5. **Virtual machines** = This uses the concept of **"Virtualization"**
6. **WSL v2** = Windows Subsystem for Linux. You can download it and use Linux without the need to use virtual machines. This is also good for low end PCs.
7. **Termux** = This is an android app, which you can use the Linux terminal on.
## Virtualization
- This is the method on how your machine allocate our memory to the virtual machines on your host machine/VMs. There are 2 types of virtualization:
1. Type-1 (Bare-Metal Hypervisor)
	- Runs directly on the physical hardware of your machine.
	- Doesn't require a host operating system.
	- Examples: **VMware ESXi, Proxmox, Xen.**
	- Advantages:
		- High Performance and Efficiency.
		- Better resource management and isolation
		- Commonly used in enterprise environments for server virtualization
2. Type-2 (Hosted Hypervisor):
	- Runs on top of a host operating system.
	- Relies on the host OS to manage hardware resources
	- Examples: **VMware Workstation, Oracle VirtualBox**.
	- Advantages:
		- Easier to set up and use
		- Suitable for personal or development environments.
## Before using virtualization, check these system settings:-
- On windows, Task Manager > Performance > CPU:
- check virtualization, if disabled you have to enable it on BIOS (Check YouTube). If enabled, you are good to go.
