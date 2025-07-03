# 🔧 01 - Linux Kernel

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Stars](https://img.shields.io/github/stars/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/stargazers)
[![Forks](https://img.shields.io/github/forks/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/network/members)

---

## 🧭 Navigation

📂 [`Main repository README`](https://github.com/AntonioJavaDeveloper/linux/blob/main/README.md)  
└── 📁 [`Chapter introduction`](./README.md)  
&emsp;&emsp;├── [`01 - Linux Kernel`](./1-kernel.md)  ← **you are here**  
&emsp;&emsp;├── [`02 - Linux Distributions`](./2-distributions.md)  
&emsp;&emsp;├── [`03 - Hands-on Lab: Kernel and Distros in Action`](./3-hands-on-summary.md)  

---

## 📚 Introduction

![Linux Kernel](https://raw.githubusercontent.com/AntonioJavaDeveloper/assets/refs/heads/main/linux/00-linux-fundamentals/linux-kernel.png)

The kernel is the core of the Linux operating system. It acts as a bridge between hardware and software, being responsible for managing essential resources such as memory, processes, devices, networks, and file systems. Without the kernel, the system would not be able to interact with the hardware in a controlled and secure manner.

Whenever an application needs access to hardware resources, it must go through the system kernel.

---

## 🧠 What Is the Kernel?

The kernel is a special program that runs in privileged mode (kernel mode: execution level with full hardware access, unlike user mode where regular applications run) and has full control over the system. It is loaded right after the bootloader (device startup) and remains running throughout the system's life.

### Main Responsibilities:

- Process management (creation, scheduling, termination)  
- Memory management (allocation, swapping, caching)  
- Device control (drivers, input/output)  
- Inter-process communication (IPC)  
- Hardware abstraction for user space

### 🧱 Types of Kernel

Linux uses a **modular monolithic** kernel model, which means it is a single binary but with support for dynamically loadable modules. In other words, the kernel can grow or shrink by enabling or disabling code chunks (modules) as needed. For more about kernel modules, see the section below `🧩 Kernel Modules`.

Other kernel categories include:

- **Monolithic**: the entire core is a single block (e.g., Linux)  
- **Microkernel**: minimal functionality in the core, everything else runs in user space (e.g., Minix)  
- **Hybrid**: mixes characteristics of both above (e.g., Windows NT)

### 📂 Where Does the Kernel Live in the System?

- The kernel binary is usually located at:
  ```
  /boot/vmlinuz-<version>
  ```

- You can check the current kernel version with:

  ```
  uname -r
  ```

### 🧪 Exploring the Kernel in Real-Time

Linux exposes kernel information via virtual file systems:

- `/proc` – Information about processes, CPU, memory, etc.  
- `/sys` – Interface with devices and kernel subsystems

Examples:

```bash
cat /proc/cpuinfo
cat /proc/meminfo
ls /sys/class/net
```

---

## 🧩 Kernel Modules

The Linux kernel is **modular**, meaning it can load and unload parts of its code as needed, without rebooting the system. These parts are called **kernel modules**.

A module is like a "plugin" that adds features to the kernel at runtime. This allows the system to be more lightweight and flexible, loading only the needed components.

### Examples of Modules:

- Device drivers (e.g., network card, USB, sound)  
- File systems (e.g., ext4, xfs, ntfs)  
- Support for network or encryption protocols

### Useful Commands:

- List loaded modules:
  ```bash
  lsmod
  ```

- Manually load a module:
  ```bash
  modprobe module_name
  ```

- Remove a module:
  ```bash
  rmmod module_name
  ```

- Get information about a module:
  ```bash
  modinfo module_name
  ```

- Kernel modules are located at:
  ```
  /lib/modules/<version>/
  ```

> 💡 Modules are stored under `/lib/modules/<kernel_version>/` and are automatically loaded depending on system or hardware requirements.

This modular architecture is one of Linux’s great advantages, as it allows the system to be adapted for different scenarios — from lightweight servers to embedded systems or hardware-specific setups.

---

## 💬 What Is the Shell?

The **shell** is a program that serves as an interface between the user and the operating system. It interprets commands typed by the user and passes them to the kernel for execution. In other words, the shell is the "translator" between you and the core of the system.

There are two main types of shell:

- **Interactive shell**: when you type commands directly in the terminal.  
- **Script shell**: when you write commands in `.sh` files for automated execution.

---

### 🐚 Most Common Shell Types

| Shell     | Typical Path        | Key Features                                                  |
|-----------|---------------------|----------------------------------------------------------------|
| `bash`    | `/bin/bash`         | The most common in Linux distros. Feature-rich.               |
| `sh`      | `/bin/sh`           | POSIX standard shell. Simple and portable.                    |
| `zsh`     | `/bin/zsh`          | Interactive, customizable, often used with Oh My Zsh.         |
| `fish`    | `/usr/bin/fish`     | Focused on usability and auto-suggestions.                    |
| `dash`    | `/bin/dash`         | Very lightweight and fast. Used during boot in some distros.  |
| `ksh`     | `/bin/ksh`          | KornShell. Historical and powerful, used in Unix environments.|

To find out which shell you’re using:

```bash
echo $SHELL
```

To list available shells on the system:

```bash
cat /etc/shells
```

### 🧪 Shell Usage Example

```bash
# Simple command
ls -lh /etc

# Basic script
#!/bin/bash
echo "Hello, world!"
```

> 💡 The shell is not part of the kernel, but it’s the main tool to interact with it — whether to run commands, automate tasks, or manage the system.

---

## 📖 Further Reading

- [Official Linux kernel documentation](https://www.kernel.org/doc/)  
- [Official Linux kernel source code repository](https://github.com/torvalds/linux)  
- `man 7 proc` – Manual page about the /proc file system  
- `man uname` – Displays system information

---

## 📬 Contributions

If this project helped or inspired you, consider leaving a ⭐ on the repository!

Feel free to open *issues* with suggestions, fixes, or questions. This repository is a space for **continuous improvement** and for consolidating best practices in using Linux as an infrastructure platform.

---

## 🔗 Quick Navigation

➡️ [Next: `02 - Linux Distributions`](./2-distributions.md)  
🔙 [Back to chapter introduction](./README.md)

---

## 📫 Contact

If you'd like to get in touch for opportunities or questions:

- 🌐 [https://javadeveloper.com.br/](https://javadeveloper.com.br/)  
- 💼 [LinkedIn](https://www.linkedin.com/in/antonio-javadeveloper/)  
- 📧 antonio@javadeveloper.com.br  

> Developed by [AntonioJavaDeveloper](https://github.com/AntonioJavaDeveloper)
