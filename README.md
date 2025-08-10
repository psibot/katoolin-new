# katoolin 3   - WORK IN PROGRESS FOR NEW MENUS
Automatically install all Kali linux tools

# Features
- Add Kali linux repositories
- Remove kali linux repositories
- Install Kali linux tools

# Requirements
- Python 3
- An operating system (tested on Ubuntu)

# ✅ Fixing GPG Key Error on Kali Linux (Modern Method)
---

````markdown

When running `sudo apt update` on Kali Linux, you might face a GPG key error like this:


Get:1 http://kali.download/kali kali-rolling InRelease [41.5 kB]
Err:1 http://kali.download/kali kali-rolling InRelease
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY ED65462EC8D5E4C5
Reading package lists... Done
W: GPG error: http://kali.download/kali kali-rolling InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY ED65462EC8D5E4C5
E: The repository 'http://http.kali.org/kali kali-rolling InRelease' is not signed.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
````

This means Kali's signing key is missing from your system.

---

## 🔧 Solution (Manual Modern Method)

Follow these steps to resolve the issue by fetching and adding the missing GPG key.

### 1. Download the GPG Key from Kali’s Official Server

```bash
curl -fsSL https://archive.kali.org/archive-key.asc -o kali-archive-key.asc
```

### 2. Add the Key to APT’s Trusted Keyring

```bash
sudo gpg --dearmor < kali-archive-key.asc | sudo tee /etc/apt/trusted.gpg.d/kali.gpg > /dev/null
```

### 3. Remove the Downloaded Key File (Optional)

```bash
rm kali-archive-key.asc
```

### 4. Update the Package List Again

```bash
sudo apt update
```

---

## ✅ Result

The update should now work without GPG key errors.

```bash
Hit:1 http://kali.download/kali kali-rolling InRelease
Reading package lists... Done
```

---

## 📌 Notes

* This method is cleaner and aligns with current best practices for GPG key management in Debian-based systems.
* Always make sure the key you're importing is from a **trusted source**.



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



