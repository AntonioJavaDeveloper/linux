# 📦 02 - Distribuições Linux

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Stars](https://img.shields.io/github/stars/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/stargazers)
[![Forks](https://img.shields.io/github/forks/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/network/members)

---

## 🧭 Navegação

📂 [`README principal do repositório`](https://github.com/AntonioJavaDeveloper/linux/blob/main/README.pt-BR.md)  
└── 📁 [`Introdução do capítulo`](./README.pt-BR.md)  
&emsp;&emsp;├── [`01 - Kernel do Linux`](./1-kernel.pt-BR.md)  
&emsp;&emsp;├── [`02 - Distribuições Linux`](./2-distributions.pt-BR.md) ← **você está aqui**    
&emsp;&emsp;├── [`03 - Laboratório Prático: Kernel e Distribuições em Ação`](./3-hands-on-summary.pt-BR.md)

---

## 📚 Introdução

![Distribuição Linux](https://raw.githubusercontent.com/AntonioJavaDeveloper/assets/refs/heads/main/linux/00-linux-fundamentals/linux-distributions.png)

O termo “Linux” é frequentemente usado para se referir a todo um sistema operacional, mas tecnicamente, **Linux é apenas o kernel** — o núcleo que faz a ponte entre o hardware e o software. Ele opera em um espaço privilegiado (Kernel Space), gerenciando recursos como CPU, memória e dispositivos.

No entanto, o que usamos no dia a dia são as **distribuições Linux**: sistemas completos que se posicionam na camada de aplicações (User Space), combinando o kernel com ferramentas, bibliotecas, ambientes gráficos, gerenciadores de pacotes e configurações específicas.

Cada distribuição é, na prática, uma **personalização da camada de software que interage com o kernel** — moldada para atender diferentes propósitos, públicos e filosofias. Algumas são otimizadas para servidores, outras para desktops, outras para containers, dispositivos embarcados ou segurança ofensiva.

---

## 🧩 O que é uma distribuição?

Uma **distribuição Linux** (ou “distro”) é um sistema operacional completo baseado no kernel Linux, que inclui:

- Gerenciador de pacotes (ex: `apt`, `dnf`, `pacman`)
- Conjunto de ferramentas GNU (ex: `bash`, `coreutils`, `grep`, `sed`)
- Ambiente gráfico (opcional)
- Scripts de inicialização e configuração
- Repositórios de software
- Documentação e suporte da comunidade

Cada distribuição toma decisões sobre quais componentes incluir, como organizá-los e como mantê-los atualizados — e é isso que define sua identidade.

---

## 🧬 Famílias de distribuições

As distribuições podem ser agrupadas em famílias, com base em sua origem:

| Família Base | Distribuições derivadas                          | Gerenciador de Pacotes  |
|--------------|--------------------------------------------------|-------------------------|
| Debian       | Ubuntu, Linux Mint, Kali, Pop!_OS                | `apt` / `dpkg`          |
| Red Hat      | Fedora, CentOS, Rocky Linux, AlmaLinux           | `dnf` / `rpm`           |
| Arch Linux   | Manjaro, EndeavourOS                             | `pacman`                |
| Slackware    | Slax, Zenwalk                                    | `pkgtool`               |
| Independente | Gentoo, Void Linux, NixOS, Alpine                | Varia                   |

> 💡 Algumas distribuições, como o Alpine Linux, também são independentes e focadas em cenários específicos como containers.

---

## 🧪 Como descobrir sua distribuição

Você pode verificar qual distribuição está usando com:

```bash
cat /etc/os-release
```

Ou, de forma mais amigável:

```bash
hostnamectl
```

---

## 🧠 Qual distribuição escolher?

A escolha da distribuição depende do seu objetivo, familiaridade e ambiente de uso:

| Cenário                        | Distribuições recomendadas                          |
|-------------------------------|-----------------------------------------------------|
| 👨‍💻 Desenvolvimento e desktop | Ubuntu, Fedora, Pop!_OS, Manjaro                    |
| 🖥️ Servidores                 | Debian, Rocky Linux, AlmaLinux, Ubuntu Server       |
| 🧪 Testes e aprendizado        | Arch Linux, Gentoo, Kali Linux                      |
| 📦 Containers e minimalismo    | Alpine Linux, Debian Slim                          |
| 🧱 Infraestrutura corporativa  | RHEL, SUSE, Oracle Linux                           |

---

## 📖 Leitura complementar

- [DistroWatch – Lista de distribuições Linux](https://distrowatch.com/)
- [Comparativo de distros no Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_Linux_distributions)
- `man os-release` – Informações sobre o arquivo de identificação da distro

---

## 📬 Contribuições

Se este projeto te ajudou ou inspirou, considere deixar uma estrela ⭐ no repositório!

Sinta-se à vontade para abrir *issues* com sugestões, correções ou dúvidas. Este repositório é um espaço voltado à **evolução constante** e à consolidação de boas práticas no uso do Linux como plataforma de infraestrutura.

---

## 🔗 Navegação Rápida

➡️ [Avançar para: `03 - Laboratório Prático: Kernel e Distribuições em Ação`](./3-hands-on-summary.pt-BR.md)  
🔙 [Voltar para: `01 - Kernel do Linux`](./1-kernel.pt-BR.md)

---

## 📫 Contato

Caso deseje entrar em contato para oportunidades ou dúvidas:

- 🌐 [https://javadeveloper.com.br/](https://javadeveloper.com.br/)
- 💼 [LinkedIn](https://www.linkedin.com/in/antonio-javadeveloper/)
- 📧 antonio@javadeveloper.com.br

> Developed by [AntonioJavaDeveloper](https://github.com/AntonioJavaDeveloper)