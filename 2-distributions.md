# 📦 02 - Linux Distributions

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Stars](https://img.shields.io/github/stars/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/stargazers)
[![Forks](https://img.shields.io/github/forks/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/network/members)

---

## 🧭 Navigation

📂 [`Main repository README`](https://github.com/AntonioJavaDeveloper/linux/blob/main/README.md)  
└── 📁 [`Chapter introduction`](./README.md)  
&emsp;&emsp;├── [`01 - Linux Kernel`](./1-kernel.md)  
&emsp;&emsp;├── [`02 - Linux Distributions`](./2-distributions.md) ← **you are here**    
&emsp;&emsp;├── [`03 - Hands-on Lab: Kernel and Distros in Action`](./3-hands-on-summary.md)

---

## 📚 Introduction

![Linux Distributions](https://raw.githubusercontent.com/AntonioJavaDeveloper/assets/refs/heads/main/linux/00-linux-fundamentals/linux-distributions.png)

The term “Linux” is often used to refer to an entire operating system, but technically, **Linux is just the kernel** — the core that bridges hardware and software. It operates in a privileged space (Kernel Space), managing resources such as CPU, memory, and devices.

However, what we use day to day are **Linux distributions**: complete systems that sit in the application layer (User Space), combining the kernel with tools, libraries, graphical environments, package managers, and specific configurations.

Each distribution is essentially a **customization of the software layer that interacts with the kernel** — tailored to serve different purposes, audiences, and philosophies. Some are optimized for servers, others for desktops, containers, embedded devices, or offensive security.

---

## 🧩 What Is a Distribution?

A **Linux distribution** (or “distro”) is a complete operating system based on the Linux kernel, which includes:

- Package manager (e.g., `apt`, `dnf`, `pacman`)
- GNU tools suite (e.g., `bash`, `coreutils`, `grep`, `sed`)
- Graphical environment (optional)
- Startup and configuration scripts
- Software repositories
- Community documentation and support

Each distribution makes decisions about what components to include, how to organize them, and how to keep them up to date — and that’s what defines its identity.

---

## 🧬 Distribution Families

Distributions can be grouped into families based on their origin:

| Base Family  | Derived Distributions                          | Package Manager     |
|--------------|------------------------------------------------|---------------------|
| Debian       | Ubuntu, Linux Mint, Kali, Pop!_OS              | `apt` / `dpkg`      |
| Red Hat      | Fedora, CentOS, Rocky Linux, AlmaLinux         | `dnf` / `rpm`       |
| Arch Linux   | Manjaro, EndeavourOS                           | `pacman`            |
| Slackware    | Slax, Zenwalk                                  | `pkgtool`           |
| Independent  | Gentoo, Void Linux, NixOS, Alpine              | Varies              |

> 💡 Some distributions, like Alpine Linux, are also independent and focused on specific scenarios like containers.

---

## 🧪 How to Identify Your Distribution

You can check which distribution you're using with:

```bash
cat /etc/os-release
```

Or, in a more user-friendly way:

```bash
hostnamectl
```

---

## 🧠 Which Distribution Should You Choose?

Choosing a distribution depends on your goal, familiarity, and usage environment:

| Scenario                        | Recommended Distributions                         |
|---------------------------------|--------------------------------------------------|
| 👨‍💻 Development & desktop        | Ubuntu, Fedora, Pop!_OS, Manjaro                  |
| 🖥️ Servers                      | Debian, Rocky Linux, AlmaLinux, Ubuntu Server     |
| 🧪 Testing & learning            | Arch Linux, Gentoo, Kali Linux                    |
| 📦 Containers & minimalism      | Alpine Linux, Debian Slim                         |
| 🧱 Enterprise infrastructure     | RHEL, SUSE, Oracle Linux                          |

---

## 📖 Further Reading

- [DistroWatch – List of Linux Distributions](https://distrowatch.com/)
- [Distro comparison on Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_Linux_distributions)
- `man os-release` – Info on the distro identification file

---

## 📬 Contributions

If this project helped or inspired you, consider leaving a ⭐ on the repository!

Feel free to open *issues* with suggestions, fixes, or questions. This repository is a space for **continuous improvement** and for consolidating best practices in using Linux as an infrastructure platform.

---

## 🔗 Quick Navigation

➡️ [Next: `03 - Hands-on Lab: Kernel and Distros in Action`](./3-hands-on-summary.md)  
🔙 [Back to: `01 - Linux Kernel`](./1-kernel.md)

---

## 📫 Contact

If you'd like to get in touch for opportunities or questions:

- 🌐 [https://javadeveloper.com.br/](https://javadeveloper.com.br/)
- 💼 [LinkedIn](https://www.linkedin.com/in/antonio-javadeveloper/)
- 📧 antonio@javadeveloper.com.br

> Developed by [AntonioJavaDeveloper](https://github.com/AntonioJavaDeveloper)
