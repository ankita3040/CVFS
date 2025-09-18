# Customised Virtual File System (CVFS)

A system-level project written in **C/C++** that simulates the functionality of a Linux-like file system.  
It provides a **custom shell interface** to perform file operations such as create, read, write, delete, and list files.

---

## Description
The **Marvellous CVFS** project is a customised implementation of a **Virtual File System**.  
It simulates the **core components of Linux file systems**, including inodes, superblock, file tables, and UAREA (User Area).  
This project helps students and developers understand how operating systems manage files internally and provides hands-on experience with **system programming**.

---

## Key Features
- **Custom Shell Interface**
  - Interactive shell (`Marvellous CVFS>`) to accept user commands.
- **Linux-like Commands**
  - `creat`, `write`, `read`, `ls`, `stat`, `unlink`, `exit`, `help`, `man`.
- **File System Simulation**
  - Inode-based file storage simulation.  
  - Superblock maintains total and free inodes.  
  - UAREA holds user-specific file descriptors.  
- **System Call Simulation**
  - Core operations (`creat`, `read`, `write`, `unlink`) mimic Linux system calls.
- **Error Handling**
  - Returns error codes for invalid parameters, insufficient space, or permission issues.
- **Learning Outcome**
  - Deep dive into **file system internals, shell design, memory management, and low-level programming**.

---

## Technologies Used
- **Language**: C / C++  
- **Platform**: Cross-platform (developed & tested on Windows/Linux)  
- **Tools**: GCC / MinGW / Visual Studio Code  

---

## Getting Started

### Dependencies
- GCC or any C/C++ compiler  
- Windows / Linux OS  
- Basic knowledge of terminal/command prompt  

### Compiling the Project
```bash
gcc CVFS.c -o Myexe
```

### Running the Project
```bash
./Myexe
```

---

## Example Usage

```bash
$ ./Myexe

Marvellous CVFS > creat Demo.txt 3
File is successfully created with FD : 0

Marvellous CVFS > write 0
Please enter data that you want to write into the file
Jay Ganesh
13 bytes get successfully written into the file

Marvellous CVFS > read 0 10
Read operation is successful
Data from file : Jay Ganesh

Marvellous CVFS > ls
Demo.txt

Marvellous CVFS > stat Demo.txt
----------statistical information of the file------------
File name : Demo.txt
File size on disk : 100
Actual file size  : 13
Link count  : 1
File Permission   : Read + Write
File Type : Regular File

Marvellous CVFS > Unlink Demo.txt
Unlink operation successfully performed

Marvellous CVFS > exit
Thank you for using Marvellous CVFS
```

---

## Help

Inside the shell, type:

- `help` → Displays all supported commands  
- `man <command>` → Displays detailed manual for a specific command  

Example:
```bash
Marvellous CVFS > man creat
Description : This command is used to create new regular file on our file system
Usage : creat File_name Permissions
```

---

## Authors
- **Ankita Anil Patil** — [@ankitapatil3040](https://github.com/ankita3040/)


---

## Version History
- **0.2** — Added read/write/stat functionality, improved error handling.  
- **0.1** — Initial release with file creation and unlink functionality.  


---

## Acknowledgments  
- Linux File System Internals — Conceptual inspiration.  
- Classic system programming resources on inodes and file management.  
