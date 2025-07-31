i want readme file on github # 🔐 Linux File Permissions - Explained and Automated with Python

This project demonstrates how Linux file permissions work and how to change them programmatically using Python. It includes a flowchart, permission breakdown, and a script to set permissions to rwxrwxr-x (775).

---

## 🧠 Understanding File Permissions

A typical Linux file permission looks like this:

rwxrwxr-x


| Section      | Meaning                       |
|--------------|-------------------------------|
| r = 4      | Read                          |
| w = 2      | Write                         |
| x = 1      | Execute                       |

### 🔍 Breakdown

- **Owner** → rwx → Full control (4+2+1 = 7)
- **Group** → rwx → Full control (7)
- **Others** → r-x → Read + execute only (4+1 = 5)

**Total numeric equivalent**: 775

---

## 📊 Flowchart
<br/> <img src="pic6.png" alt="Script Content" width="500"/> </div>


## The python example
i create a python file on virtual box inside ubento by writing in terminal the code is write my name in example.txt 
<div align="center"> <img src="pic1.png" alt="Creating Python File" width="500"/> <br/> <img src="pic4.png" alt="Script Content" width="500"/> </div>

after that i run the code and use command ls to cheackout if the premmiton has changed or not 
<div align="center"> <img src="pic3.png" alt="Creating Python File" width="500"/> <br/> <img src="pic2.png" alt="Script Content" width="500"/> </div>

---
## the code 
```
import os

file_path = "example.txt"
with open(file_path, "w") as file:
    file.write("Khalid")

os.chmod(file_path, 0o775)

print(f"Permissions for '{file_path}' changed to rwxrwxr-x (775)
```
