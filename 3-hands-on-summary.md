# 🧪 03 - Hands-on Lab: Kernel and Distros in Action

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Stars](https://img.shields.io/github/stars/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/stargazers)
[![Forks](https://img.shields.io/github/forks/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/network/members)

---

## 🧭 Navigation

📂 [`Main repository README`](https://github.com/AntonioJavaDeveloper/linux/blob/main/README.md)  
└── 📁 [`Chapter introduction`](./README.md)  
&emsp;&emsp;├── [`01 - Linux Kernel`](./1-kernel.md)  
&emsp;&emsp;├── [`02 - Linux Distributions`](./2-distributions.md)    
&emsp;&emsp;├── [`03 - Hands-on Lab: Kernel and Distros in Action`](./3-hands-on-summary.md) ← **you are here**  

---

## 📚 Introduction

This hands-on lab aims to demonstrate, in a practical way, the application of the concepts covered in this chapter — focusing on kernel identification, module handling, and distro recognition in different environments.

Two virtual environments provisioned with Vagrant will be used:

- 🐧 Ubuntu (Debian-based)
- 🐮 Rocky Linux (Red Hat-based)

The required configuration files are already available in the `vagrant` directory at the repository root. No need to write the code manually — just run the indicated commands to start the environments and perform the proposed tests.

```
📁 vagrant/
└── 📁 ubuntu/
    └── Vagrantfile
└── 📁 rocky/
    └── Vagrantfile
```

You will be able to run real commands to:

- Check the kernel version
- Explore kernel modules
- Identify the current distribution
- Test basic commands using `apt` and `dnf`

---

## 🚀 Starting the environments with Vagrant

Create two Vagrantfile files, each within its respective directory.

### 📄 `vagrant/ubuntu/Vagrantfile`

```ruby
Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-22.04"
  config.vm.hostname = "ubuntu-lab"
  config.vm.network "private_network", type: "dhcp"
  config.vbguest.auto_update = false

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.cpus = 1
    vb.name = "ubuntu"
  end
end
```

### 📄 `vagrant/rocky/Vagrantfile`

```ruby
Vagrant.configure("2") do |config|
  config.vm.box = "generic/rocky9"
  config.vm.hostname = "rocky-lab"
  config.vm.network "private_network", type: "dhcp"
  config.vbguest.auto_update = false

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.cpus = 1
    vb.name = "rocky"
  end
end
```

To start the environments, navigate to the appropriate directory and run the commands below.

### 🐧 Ubuntu

```bash
cd vagrant/ubuntu
vagrant up
vagrant ssh
```

### 🐮 Rocky Linux

```bash
cd vagrant/rocky
vagrant up
vagrant ssh
```

---

## 📂 Checking the Kernel

| Command                    | Description                         | Expected Output (example)    |
|----------------------------|-------------------------------------|------------------------------|
| `uname -r`                 | Kernel version                      | `5.15.0-105-generic`         |
| `ls /boot`                 | Kernel-related files                | `vmlinuz`, `initrd.img`      |
| `cat /proc/version`        | Detailed kernel info                | Kernel + compiler info       |

---

## 🧩 Exploring Modules

| Command                    | Description                         |
|----------------------------|-------------------------------------|
| `lsmod`                    | List loaded modules                 |
| `modinfo <module>`         | Show info about a module            |
| `modprobe <module>`        | Load a module manually              |
| `rmmod <module>`           | Remove a module                     |

---

## 🧠 Identifying the Distribution

| Command                    | Ubuntu                             | Rocky Linux                  |
|----------------------------|-------------------------------------|------------------------------|
| `cat /etc/os-release`      | `Ubuntu 20.04`                      | `Rocky Linux 9`              |
| `hostnamectl`              | Shows name, kernel, OS info         | Shows name, kernel, OS info  |

---

## 📦 Testing the Package Manager

| Action                     | Ubuntu (APT)                        | Rocky (DNF)                  |
|----------------------------|-------------------------------------|------------------------------|
| Update package list        | `sudo apt update`                  | `sudo dnf check-update`     |
| Install `curl` package     | `sudo apt install htop`            | `sudo dnf install htop`     |
| Remove `curl` package      | `sudo apt remove htop`             | `sudo dnf remove htop`      |

> ⚠️ This lab does not replace the dedicated chapters on package management. The focus here is to validate the environment and reinforce kernel and distribution concepts.

---

## 🛑 Shutting Down the Environment

After completing the lab tests, it's recommended to remove the provisioned environments to free up system resources. Below are the commands to destroy the virtual machines and optionally remove the boxes.

### 🧹 Destroying the virtual machines

In each directory (vagrant/ubuntu and vagrant/rocky), run the command below to remove the virtual machines:

```bash
vagrant destroy -f
```

> 💡 The `destroy` command deletes the created VM but keeps the base box locally, allowing for fast recreation later without a new download.

---

### 🗑️ Removing Downloaded Boxes

To free up disk space if you don’t plan to reuse the boxes:

```bash
# List all installed boxes
vagrant box list

# Remove the boxes used in this lab
vagrant box remove bento/ubuntu-22.04
vagrant box remove generic/rocky9
```

> ⚠️ Removing boxes means the files will be downloaded again next time you run `vagrant up`.

---

## 📖 Further Reading

- [Vagrant Documentation](https://developer.hashicorp.com/vagrant/docs)
- `man uname`, `man modprobe`, `man os-release`

---

## 📬 Contributions

If this project helped or inspired you, consider leaving a ⭐ on the repository!

Feel free to open *issues* with suggestions, fixes, or questions. This repository is a space for **continuous improvement** and for consolidating best practices in using Linux as an infrastructure platform.

---

## 🔗 Quick Navigation

➡️ [Next chapter: `01 - Linux Directory Structure`](https://github.com/AntonioJavaDeveloper/linux/blob/01-fhs/README.md)  
🔙 [Back to: `02 - Linux Distributions`](./2-distributions.md)

---

## 📫 Contact

If you'd like to get in touch for opportunities or questions:

- 🌐 [https://javadeveloper.com.br/](https://javadeveloper.com.br/)
- 💼 [LinkedIn](https://www.linkedin.com/in/antonio-javadeveloper/)
- 📧 antonio@javadeveloper.com.br

> Developed by [AntonioJavaDeveloper](https://github.com/AntonioJavaDeveloper)
