# 🐧 Linux as an Infrastructure Platform: Fundamentals, Automation, and Best Practices

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE) [![Stars](https://img.shields.io/github/stars/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/stargazers) [![Forks](https://img.shields.io/github/forks/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/network/members)

This repository presents a collection of essential solutions, practices, and concepts for building, managing, and automating environments based on **Linux**. Each branch covers a specific aspect of the operating system — such as permissions, processes, networking, security, integration with automation tools, among others.

The practical examples are organized modularly and, when applicable, implemented in **Java**, demonstrating how general-purpose programming languages can interact with the operating system for tasks like file handling, command execution, and resource monitoring.

To facilitate scenario reproduction, each chapter includes configurable environments using **Vagrant** — allowing anyone to run the examples in an isolated and controlled manner without relying on the host machine configuration. However, Vagrant usage is optional: the main focus is on concepts and practices that can be applied across any Linux distribution.

The goal is to offer a solid and reusable reference for professionals working in infrastructure, DevOps, or backend development — with a focus on clarity, efficiency, and best practices.

---

## ⚙️ Requirements

To run the example environments provided in this repository, you’ll need the following tools installed on your local machine:

* [**Oracle VirtualBox**](https://www.virtualbox.org/) – Free hypervisor used as the default provider for virtual machines.
* [**Vagrant**](https://www.vagrantup.com/) – Automation tool for provisioning and managing development environments.

> 💡 These tools are only recommended if you wish to run the examples locally. The conceptual content and code snippets can be understood independently of the practical execution.

---

## 🗂️ Chapter Organization

This repository is structured in **thematic chapters**, each addressing a specific aspect of the Linux operating system. To keep the content modular and version-controlled, **each chapter is located in a separate branch**.

### 📌 Branch Structure

* The `main` branch acts as the central index of the project. It contains both `README.md` files (in English and Portuguese), along with general requirements and navigation guidance.
* Each chapter resides in its own branch, named using a numeric prefix and a descriptive English identifier (e.g., `01-fhs`, `02-boot-process`, `03-systemd`).
* Within each branch, multiple `README.md` files may exist to cover different sections or subtopics.
* All documentation files are provided in **Portuguese (`README.pt-BR.md`)** and **English (`README.md`)**.

### 🧭 Navigating Between Chapters

At the end of the `README.md` in the `main` branch, you’ll find the **📚 Chapter Catalog** section, which lists all the topics covered in this repository. Each row of the table contains the chapter title and a direct link to the respective content, making it easy to jump between topics.

Sample navigation structure:

| Chapter                              | Link to English content                                                                              |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| 01 - Linux Directory Structure       | [📘 `01-fhs`](https://github.com/AntonioJavaDeveloper/linux/blob/01-fhs/README.md)                   |
| 02 - System Boot Process             | [📘 `02-boot-process`](https://github.com/AntonioJavaDeveloper/linux/blob/02-boot-process/README.md) |
| 03 - Service Management with systemd | [📘 `03-systemd`](https://github.com/AntonioJavaDeveloper/linux/blob/03-systemd/README.md)           |

> 💡 The table above provides a summary of available chapters. To access any chapter, just click the corresponding link — you’ll be redirected to the specific branch on GitHub without needing to clone the repository or use Git commands.

> The complete list of all chapters can be found in the **📚 Chapter Catalog** section at the end of this file.

---

## 📚 Chapter Catalog

| Chapter                              | Link to English content                                                                              |
| ------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| 01 - Linux Directory Structure       | [📘 `01-fhs`](https://github.com/AntonioJavaDeveloper/linux/blob/01-fhs/README.md)                   |
| 02 - System Boot Process             | [📘 `02-boot-process`](https://github.com/AntonioJavaDeveloper/linux/blob/02-boot-process/README.md) |
| 03 - Service Management with systemd | [📘 `03-systemd`](https://github.com/AntonioJavaDeveloper/linux/blob/03-systemd/README.md)           |

---

## 📬 Contributions

If this project helped or inspired you, consider leaving a star ⭐ on the repository!

Feel free to open *issues* with suggestions, corrections, or questions. This repository is a space for **continuous improvement** and the consolidation of best practices in using Linux as an infrastructure platform.

---

## 🔗 Quick Navigation

➡️ [Go to `01 - Linux Directory Structure`](https://github.com/AntonioJavaDeveloper/linux/blob/01-fhs/README.md)

---

## 📫 Contact

If you’d like to get in touch for opportunities or questions:

* 🌐 [https://javadeveloper.com.br/](https://javadeveloper.com.br/)
* 💼 [LinkedIn](https://www.linkedin.com/in/antonio-javadeveloper/)
* 📧 [antonio@javadeveloper.com.br](mailto:antonio@javadeveloper.com.br)

> Developed by [AntonioJavaDeveloper](https://github.com/AntonioJavaDeveloper)
