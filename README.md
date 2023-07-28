# katoolin 2 - WORK IN PROGRESS FOR NEW MENUS
Automatically install all Kali linux tools

# Features
- Add Kali linux repositories
- Remove kali linux repositories
- Install Kali linux tools

# Requirements
- Python 2.7
- An operating system (tested on Ubuntu)
  
# Need Python2

- wget https://www.python.org/ftp/python/2.7.9/Python-2.7.9.tgz
- sudo tar xzf Python-2.7.9.tgz
- cd Python-2.7.9
- sudo ./configure --enable-optimizations
- sudo make altinstall

# Installation
- sudo su
- git clone https://github.com/psibot/katoolin-new.git  && cp katoolin-new/katoolin.py /usr/bin/katoolin
- chmod +x /usr/bin/katoolin
- sudo katoolin 


# Usage
- Typing the number of a tool will install it
- Typing 0 will install all Kali Linux tools
- back : Go back
- gohome : Go to the main menu
- By installing armitage , you will install metasploit

# Warning
Before updating your system , please remove all Kali-linux repositories to avoid any kind of problem .



