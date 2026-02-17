## Overview of tools in kali linux
**1. Information gathering** = Tools for information gathering in systems, network and host. <br>
**2. Vulnerability Analysis** = Tools for finding vulnerabilities <br>
**3. Web application analysis** = Tools for finding vulnerabilities and exploits on websites. <br>
**4. Database Assessment** = Tools for finding vulnerabilities and exploits in databases. <br>
**5. Password attacks** = Tools for exploiting passwords for login, websites, applications and windows. <br>
**6. Wireless Attacks** = Tools for exploiting wireless systems like Wi-Fi and Bluetooth. <br>
**7. Reverse Engineering** = Tools for exploiting softwares, mobile apps and binary files. <br>
**8. Exploitation tools** = tools for exploiting softwares, mobiles, computers, websites and any things. <br>
**9. Sniffing and spoofing** = tools for listening or hijacking networks. <br>
**10. Post exploitation** = tools for maintaining our access. Used after exploiting a system. <br>
**11. Forensics** = Tools for doing researches and investigate cyber-attacks. <br>
**12. Reporting tools** = tools for reporting preparation. after some forensic you will report and these tools will help you. <br>
**13. Social Engineering tools** = Tools used for social engineering attacks. <br>
**14. System services** = buttons used to start some services. <br>
**15. Usually used apps** = softwares for some basic purposes. <br>

## Linux commands
- Linux commands uses shell. The shell helps us to communicate with the kernel and helps to execute codes. it is also called the **terminal**.
- The terminal have 5 parts:
	- Username = rexder
	- Hostname = HunterMachine
	- Current Directory = PATH (~)
	- Privilege = $ - user, # - root.
	- Command Place = after the '$' or '#'
- Home directory is denoted by '~'.
- Local directory is denoted by '.'.
- All directories is denoted by 'star symbol'.

### Linux command basics
- On Linux there are over 1000 commands, but we are expected to know the main and useful ones only.
- Also those commands have their own **options** and **arguments**.
- A command is a small program that do one task well.
 
#### grep - global search for regular expression
- `grep [options] pattern [files]`.
- The grep filter searches file for a particular pattern of characters, and displays all lines that contain that pattern. The pattern that is searched in the file is referred to as the regular expression (grep stands for global search for regular expression and print out).
- grep command options:
	- `grep -i 'search' file` = case insensitive.
	- `grep -c 'search' file` = count numbers line.
	- `grep -l 'search'` = displays file name.
	- `grep -r 'search' folder_name` = search text in folders.
	- `grep -v 'search' file_name` = to display without the term.
	- `grep -n 'search' file` = to display the term and find line number.
	- `grep -o 'pattern' file_name` = to display that specific word only.

#### Wc - Word count
- Synopsis = `wc [option] [file]`
- It is used to find out numbers of lines, word count, byte and characters count in the files specified in the arguments..
	- Line (-l) = shows the number of lines
	- word (-w) = shows the word count
	- byte (-c) = shows the size of the of the file in bytes.

### Multiple command executions
- You can run/execute multiple commands in 1 line
- Using 3 methods:
	- and (&&) = Think of this like a logic operator.
	- or ( || ) = Think of this like a logic operator.
	- piping ( |\) = Takes the output of the first command and then use it as input for the second command.

#### Sed / Stream Editor
- A powerful command-line tool for parsing and transforming text in linux.
- processes files line by line , making it efficient for large text processing tasks.
- Common uses:
	- Text substitution and replacement
	- Deleting or selecting specific lines.
	- Efficient text manipulation for tasks like network information gathering or penetration testing logs.
- Syntax: `sed [options] 'command' file`.
	- substitute (replace) = `sed 's/old/new' file`.
	- You can use the ' | ' sign instead of the ' /  ' sign when using this command.
	- Use 'g' on the end to replace if it finds the word more than one time in one line.
		- `sed 's/old/new/g'`.
	- to delete = `sed '/pattern/d' file`.
 
#### awk
- a versatile command-line text-processing tool.
- Ideal for pattern scanning and data extraction in structured text.
- Named after its creators: **Aho, Weinberger and Kernighan**.
- Features:
	- Processes text line-by-line.
	- Supports complex pattern matching.
	- Allows field-based text manipulation, making it great for column based data like CSV files.
- Basic Syntax:

	```bash
	awk 'pattern { action }' file.txt.
	awk '{print $1, $3}' file.txt = prints columns 1 and 3.
	awk '/pattern/ {print$0}' file.txt = prints lines matching "pattern".
	```

- Awk by default determine columns if they are separated by space( ), Here space in known as ==delimiter==.
	- To change separator '-F' sign.
- Built-in variables
	- $0 = Entire line of text.
	- $1, $2 = represents each column (field) in a line.
	- NR = Line (record) number.
	- NF = Number of fields in the current record.
- You can use it with file or piped:

	```bash
	awk 'options' file.txt = used with files.
	cat 'file.txt' | awk 'options' = used with piping.	
	```
