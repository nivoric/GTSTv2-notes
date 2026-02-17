# GTSTv2 Cybersecurity course
### Topics to be covered during this course
#### Season-1
 - [ ] **Intro to ethical hacking** 
 - [ ] **Linux**
 - [ ] **Python**
 - [ ] **Bash**
 - [ ] **Networking**
#### Season-2
- [ ] **Footprinting and recon**
- [ ] **Scanning Networks**
- [ ] **Malware Threats**
- [ ] **Social Engineering (social media hacking)**
- [ ] **Steganography and Cryptography**
- [ ] **Network hacking**
- [ ] **System Penetration Testing (Phone, computer, server hacking)**
- [ ] **DOS/DDOS + Anonymity**
- [ ] **Website security**
- [ ] **Capture the flag (CTF)**
- [ ] **Bug bounty hunting**
- [ ] **Report and documentation**
## What you have to know?
1. You don't hack just because you know hacking concepts = You have to be very practical, we learn both concepts and practical but if you skip the practical part. sorry for you.
2. You don't be a hacker in 1 night or with class notes only
3. Don't be afraid to learn new things/concepts
4. Try to simplify everything as much as possible, don't make things hard
5. Things that seem useless have purpose
6. Always learn new things, this is still a growing field.

## Note taking softwares
1. **Git and GitHub**
- Git is a version control system tool.
- Simply, a tool to manage changes on your files version.
- Saves the files locally or on a remote server (GitHub/GitLab)
- Made by Linux development community
- GitHub is a web site/server which your git files get hosted on. Your files will be stored in a folder called "repository".

### Common terms in git
- **Push**:- is an action done when use try to upload his data to the remote git server (GitHub/GitLab/Gogs).
- **Pull**:- is an action done when user try to download some changes and integrate to the previous local repository.
- **Clone**:- is an action done when user try to download a new repository (in general, to download a repository to your local storage)
- **Commit**:- a fundamental operation that saves your changes to the repository allowing you to maintain a history of your project. Each commit is identified by a unique random string.
- **Add**:- the process of staging changes in your working repository to be included in the next commit.

### Git commands
```bash
For first time:
cd Desktop
mkdir gtst && cd gtst
git init - initiates git in the selected directory
git config --global user.name <Your username>
git config --global user.email <Your email>

for normal works:
git status
git add .
git commit -m <your commit message>
git log

For GitHub
git remote add origin <repository URL>
git push -u origin master/main (based on the branch the repo is found on) = This will ask you for your username and password (token)
git clone <your project link>
```

### Getting your token (includes pushing your notes/code into GitHub)
- Just follow these steps:-
1. create a folder with any name you like

2. initialize git = `git init`

3. add your username and email = 
    ```bash
    git config --global user.name <YOUR USERNAME>
    git config --global user.email <YOUR EMAIL>
    ```
4. Create a note on your machine like "note1.md"

5. Check the status = `git status`

6. stage the changes = `git add .`

7. commit the changes = `git commit -m <your commit message>`. You can recheck the status after this step.

8. check the logs = `git log`. You can also see any other commits done before on the selected repository.

9. create a repo on github, make it public for easier use.

10. add your repo link = `git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git`. This means that the copied repo is where notes are going to be pushed

11. Go to settings > developer settings > generate personal tokens > choose the classic one > enable all options > generate the token and copy it > save somewhere safe, you might need it again

12. Push your files to github = `git push -u origin main/master`
    Username = YOUR GITHUB USERNAME
    Password = the copied token

And then all is done! This is how you push your files to GitHub.

- When you want to push your notes again on the same repo;
1. Check status, stage the changes, commit and then pull the repo using:- `git pull origin main/master --rebase`
2. Then you push the changes to your repo
- And done, your notes are pushe to your repo.

## Another software you can use to take notes is, 
2. Obsidian: This software lets you take notes in markdown file format, which is the default file format that github uses.
3. VScode: You can also write notes on VScode in the markdown file format. You can also commit your notes from VSCode to GitHub.
4. GitHub Desktop:- You can also this app to quickly get the links of your repos with out opening your browser. Only have windows and MacOS versions.
- Also, if you are not comfortable with the whole pushing your notes to GitHub through the git CLI or from the terminal, You can just go to GitHub's website and then drag and drop the files you want to push to repos.
## Another software you can use to take notes is, 
2. Obsidian: This software lets you take notes in markdown file format, which is the default file format that GitHub uses.
3. VScode: You can also write notes on VSCode in the markdown file format. You can also commit your notes from VSCode to GitHub.
4. GitHub Desktop:- You can also this app to quickly get the links of your repos with out opening your browser. Only have windows and MacOS versions.
- Also, if you are not comfortable with the whole pushing your notes to GitHub through the git CLI or from the terminal,You can just go to GitHub's website and then drag and drop the files you want to push to repos.
# Introduction to Cybersecurity
- **Cybersecurity** is a very wide field in the IT/Information Technology world.
- It is the practice of protecting systems, networks and programs from digital attacks.
- These cyber-attacks are usually aimed at accessing, changing or destroying sensitive information; extorting money from users via ransomware or interrupting normal business processes.
- Those cyber-attacks are called hacking (non-ethical hacking to be specific)
## What is Hacking?
- **Hacking** is referred to exploiting system vulnerabilities and compromising security controls to gain unauthorized access to the system.
- *Ethical Hacking finds the weak points of loopholes in a computer, web apps or networks and reports them to the organization.*
- There person who perform hacking is called a "Hacker".
- **Vulnerability** = the quality or state of being exposed to the possibility of being attacked or harmed, either physically or emotionally.
### Types of hackers 
-  based on ethics:
1. **Black Hat Hackers** = The most evil and bad people in the cyberspace.
2. **White Hat Hackers** = The helping and good people.
3. **Grey Hat Hackers** = Individuals who sometimes act ethically and other times act unethically or engage in questionable or illegal activities.
-  Based on skill:
1. **Newbie/Noob** = Don't have any knowledge about hacking.
2. **Script Kiddie** = a script kiddie, kiddie or a skid is a relatively unskilled individual who uses scripts or programs developed by others, primarily for malicious purposes. They have better knowledge than newbies/noobs.
3. **Hacker** = Perfectly skilled, with less experience. Better than both skids and newbies.
4. **Elite/Pro Hacker** = Perfectly skilled, with much more experience. Better than all the other guys above, Maybe the best.
### Why do we learn Cybersecurity?
1. To prevent hackers from gaining unauthorized access.
2. To uncover vulnerabilities.
3. To strengthen the organization.
4. To safeguard the data.
5. To avoid security breaches.
6. To enhance security awareness.
7. The industry needs Cybersecurity experts.
### Why hack happens?
- **ATTACKS** = MOTIVE/GOAL + METHOD + VULNERABILITY.
- **MOTIVE** = Information theft, manipulating data, Financial loss, Revenge, Ransom, Damaging Reputation.
## Elements of Information security
### The CIA Triad
- The three letters in "CIA Triad" stand for **Confidentiality(Mistrawinet), Integrity(Tamagninet) and Availability(Tegegninet)**.
- The CIA Triad is a common model that forms the basis for the development of security systems.
- All security measures are based on one or more of these three principles.

1. **Confidentiality** = involves the effort of an organization to make sure data is kept secure or private. To accomplish this, access to information must be controlled to prevent the unauthorized sharing of data - whether intentional or accidental. example:
    - *Those who work with an organization's finances should be able to access the spreadsheets, bank accounts, and other information related to flow money. but the vast majority of employees, even some executives, shouldn't have the access to such information.*
    - Example of a cyber-attack = **Facebook data breach exposing user info**
2. **Integrity** = involves making sure your data is ==trustworthy and free from tampering/change==. The integrity of your data is maintained only if the data is authentic, accurate and reliable.
	- Example = *If your company provides information about senior managers on your website, this information needs to have integrity otherwise it is a big lie.*
	- Example of cyber-attack = attack on financial transactions to alter records.
3. **Availability** = means information resources (like computer hardware, software, network and date, etc...) are accessible when you need them. Even if data is kept confidential and its integrity is maintained, it is often useless unless useful to authorized personnel.
	- Example = *There is a power outage and there is no disaster recovery system in place to help users regain access to critical systems, availability will be compromised.*
	- Example of cyber-attack = cyber-attacks on a government's website causing downtime.
### Skills required to be a hacker
1. **computer programming**
2. **Computer Networking**
3. **Systems Understanding** = Linux/Windows.
- The above points are the basics but most people skip them and jump straight into hacking.
### Phases of Hacking
1. **Reconnaissance** = Gathering information about the target through passive and active means (e.g. scanning, OSINT).
2. **Scanning** = Identify open ports, services and vulnerabilities using hacking tools like Nmap.
3. **Gaining Access** = Exploiting vulnerabilities to access the target system.
4. **Maintaining access** = Establishing backdoors or persistence for continuous access.
5. **Covering tracks** = Erasing logs and hiding any signs of intrusion.
## Penetration Testing aka PenTesting
- Penetration Testing is a method of evaluating the security of an information system or network by ==simulating an attack== to:
	- Find vulnerabilities
	- Security measures
	- Documentation and Report Preparation.
### Why do we need PenTesting?
- Identification of threats
- Security Protections and controls
- Assessment of organization's security
- Evaluation of Network security
- Upgrade of Infrastructure
### Types of PenTesting
1. **Black Box PenTesting**:
	- Testing system without prior knowledge.
	- You test as an attacker.
2. **White Box PenTesting**:
	- Testing system with prior knowledge
	- You test as a Developer
3. **Grey Box PenTesting**:
	- Testing system with Limited knowledge.
	- You test as an user.
## Cybersecurity field terms
- **Red Teaming/Offensive Security** = Red Teaming involves simulating real-world attacks to test an organization's security posture.
- **Blue Teaming/Defensive Security** = Blue Teaming refers to defending against attacks and improving security controls. The Blue Team monitors systems, analyzes network traffic, and responds to potential threats.
- **Security Audit** = A security audit is a comprehensive evaluation of an organization's information systems, security controls and procedures.
- **Vulnerability Assessment** = A Vulnerability assessment identifies and classifies security flaws in systems, networks and software. In involves automated scanning, manual testing and analysis to highlight weakness.
### Jobs in Cybersecurity
- Cybersecurity expert
- Security/SOC Analyst
- Cybersecurity Consultant
- Web Penetration Tester
- Mobile Penetration Tester
- Internal and External Penetration Tester
- Network Security Tester
- Bug Bounty Hunter
### Ethics of Cybersecurity
1. Respect the privacy of others
2. Think before you type something
3. With great power comes great responsibility
- **Ethics** is the most important concept in cybersecurity, This is what differentiate good hackers from bad hackers. We have to be ethical on every approach we are working on. A single bypass can make your life at risk. SO, ALWAYS HAVE PERMISSION
- But the only way to protect your device is by thinking like a black hat.
