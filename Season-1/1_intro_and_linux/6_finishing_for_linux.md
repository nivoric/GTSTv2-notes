## Script installation
- Some hacking tools are developed by some people and these people make it open-source. So we can download and use it.
- For this purpose git have a feature called 'clone'.
```bash
git clone <link_of_the_script_from_github>
```
### Script modules
- Scripts are made with scripting languages like **python, bash, go, ruby and much more**. So when we use these programming languages to do tasks, there is something called modules/libraries.
- **Modules/Libraries** are needed to run the script as the dependencies.
```bash
Python = pip install <module_name>
Go = go install <module_name>
Ruby = gem install <module_name>
```
- If you need any help with linux commands = `man <command_name>`.
- some commands have help option:
	- `<your_command> -h`, 
	- `<your_command> -help` or
	- `<your_command> --help`.
## Linux processes and services
- **Processes**: 
	- Running instances of programs. 
	- When you execute a program like opening a text editor, running a command, or starting a web browser, Linux loads that program into memory and starts it as a process
- **Services**:
	- Background programs that start automatically or manually. Often for system tasks (also known as ==daemons==).
	- A service that runs to gather any change on the system or to count time runs on background.
- To get processes running = `ps [options]`.
- More commands:
	- `ps` -> for process running on my shell.
	- `ps -A` -> view all running processes.
	- `ps -u username` -> view user processes.
### Managing processes
- To stop process: =
	- `kill [options] [PID]`. 
	- `kill all [program_name]`.
- More on kill command:
```bash
kill -19 [PID] = to stop the process.
kill -18 [PID] = to resume the process we stopped.
kill -9 [PID] = to stop the process immediately.
...
there are 31 options.
```
- **PID** = Process ID.
- **PPID** = Parent Process ID.
- Programs where you can see the process running on your Linux machine are **top, btop (much cooler) and htop (more colors)**.
```bash
sudo apt install htop btop -y
```
### Managing Services
- Services can be started and stopped.
- We will see different hacking services for the future classes.
- To manage services, we can use tools called, "systemctl" or "service".
- syntax:
```bash
sudo systemctl start <service_name> = start the service.
sudo systemctl stop <service_name> = stop the service.
sudo systemctl status <service_name> = to check status of the service.
sudo systemctl enable <service_name> = to make it start service when the computer boots.
sudo systemctl disable <service_name> = to make it stop the service from running when the computer boots.
sudo service <service_name> start 
sudo service <service_name> stop 
```
## Null device
- /dev/null - Redirects output to nowhere.
- If you want to ignore output, you can send it to the null device, /dev/null.
- The null device is a special file that throws away whatever is fed to it. You may hear people refer to it as the bit bucket.
- If you do not want to see errors on your screen and you do not want to save them to a file, you can redirect them to `/dev/null`.
- On shell output, **there are 2 things**:
	- STDERR = 2
	- STDOUT = 1
```bash
command 2> file_name = to redirect the errors from a command result.
command 1> file_name = to redirect the error-free output.
command 2> /dev/null = to redirect our command output to /dev/null.
```
## alias
- used to give a name/shortcut to some bunch of commands.
```bash
alias rex='ls -la'
This shortcut called 'rex' will run the command 'ls -la' by just typing 'rex' in the command line
```
- But just doing this won't work for you after restarting your computer. If you want to save it into your computer:
```bash
# ~/.zshrc or ~/.bashrc or ~/.config/fish/config.fish
# add these under alias
alias rex='ls -la'
# you can add shortcuts as much as you want.
```
## Tmux - Terminal multiplier
- Tmux is used to classify our terminal work.
- You can install it using apt and it's built-in on kali-linux
```bash
sudo apt install tmux -y

# to create a config file
nano tmux.conf

# Type this
unbind C-b
unbind l
set -g prefix C-a
unbind %
bind e split-window -h
bind o split-window -v
set -g base-index 1
setw -g pane-base-index 1
# save, exit tmux and then open tmux again.
```
## Wget
- is a tool to download files from websites/servers.
```bash
wget[options][link]

wget https://tldp.org/LDP/intro-linux/intro-linux.pdf
```
## find
- On terminal, if you want to search for files, folders, music, videos or anything else, you can use the **find command**.
- it is a very essential tool.
```bash
# main syntax
find[search_path][options][search_word]

# more commands
find / -name "linux"
find /home -perm 777
find -type f | find -type d
find / -type f -perm /4000
```
- This is the end for linux.
