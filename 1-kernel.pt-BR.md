# 🔧 01 - Kernel do Linux

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Stars](https://img.shields.io/github/stars/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/stargazers)
[![Forks](https://img.shields.io/github/forks/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/network/members)

---

## 🧭 Navegação

📂 [`README principal do repositório`](https://github.com/AntonioJavaDeveloper/linux/blob/main/README.pt-BR.md)  
└── 📁 [`Introdução do capítulo`](./README.pt-BR.md)  
&emsp;&emsp;├── [`01 - Kernel do Linux`](./1-kernel.pt-BR.md)  ← **você está aqui**    
&emsp;&emsp;├── [`02 - Distribuições Linux`](./2-distributions.pt-BR.md)  
&emsp;&emsp;├── [`03 - Laboratório Prático: Kernel e Distribuições em Ação`](./3-hands-on-summary.pt-BR.md)  

---

## 📚 Introdução

![Kernel Linux](https://raw.githubusercontent.com/AntonioJavaDeveloper/assets/refs/heads/main/linux/00-linux-fundamentals/linux-kernel.png)

O kernel é o núcleo do sistema operacional Linux. Ele atua como uma ponte entre o hardware e o software, sendo responsável por gerenciar recursos essenciais como memória, processos, dispositivos, redes e sistemas de arquivos. Sem o kernel, o sistema não teria como interagir com o hardware de forma controlada e segura.

Quando algum aplicativo precisar de algum recurso do hardware, necessariamente deverá passar pelo kernel do sistema.

---

## 🧠 O que é o Kernel?

O kernel é um programa especial que é executado em modo privilegiado (modo kernel: nível de execução com acesso total ao hardware, diferente do modo usuário, onde rodam os aplicativos comuns) e tem controle total sobre o sistema. Ele é carregado logo após o bootloader(após a inicialização do dispositivo) e permanece em execução durante toda a vida do sistema.

### Principais responsabilidades:

- Gerenciamento de processos (criação, escalonamento, finalização)
- Gerenciamento de memória (alocação, swap, cache)
- Controle de dispositivos (drivers, entrada/saída)
- Comunicação entre processos (IPC, Inter-Process Communication)
- Abstração de hardware para o espaço de usuário

### 🧱 Tipos de Kernel

O Linux utiliza um modelo de kernel **monolítico modular**, o que significa que ele é um único código binário, mas com suporte a módulos carregáveis dinamicamente, ou seja, o kernel pode crescer ou diminuir habilitando ou desabilitando pedaços de códigos(módulos) conforme a necessidade. Para saber mais sobre módulos do kernel veja a seção abaixo `🧩 Módulos do Kernel`.

Outras categorias de kernel incluem:

- **Monolítico**: todo o núcleo é um único bloco (ex: Linux)
- **Microkernel**: funcionalidades mínimas no núcleo, o restante roda em espaço de usuário (ex: Minix)
- **Híbrido**: mistura características dos dois anteriores (ex: Windows NT)

### 📂 Onde o Kernel vive no sistema?

- O binário do kernel geralmente está localizado em:
  ```
  /boot/vmlinuz-<versão>
  ```

- Você pode verificar a versão do kernel atual com:

  ```
  uname -r
  ```

### 🧪 Explorando o Kernel em tempo real

O Linux expõe informações do kernel por meio de sistemas de arquivos virtuais:

- `/proc` – Informações sobre processos, CPU, memória, etc.
- `/sys` – Interface com dispositivos e subsistemas do kernel

Exemplos:

```bash
cat /proc/cpuinfo
cat /proc/meminfo
ls /sys/class/net
```

---

## 🧩 Módulos do Kernel

O kernel do Linux é **modular**, o que significa que ele pode carregar e descarregar partes do seu código conforme necessário, sem precisar reiniciar o sistema. Essas partes são chamadas de **módulos do kernel**.

Um módulo é como um “plugin” que adiciona funcionalidades ao kernel em tempo de execução. Isso permite que o sistema seja mais leve e flexível, carregando apenas os componentes necessários.

### Exemplos de módulos:

- Drivers de dispositivos (ex: placa de rede, USB, som)
- Sistemas de arquivos (ex: ext4, xfs, ntfs)
- Suporte a protocolos de rede ou criptografia

### Comandos úteis:

- Listar módulos carregados:
  ```bash
  lsmod
  ```

- Carregar um módulo manualmente:
  ```bash
  modprobe nome_do_modulo
  ```

- Remover um módulo:
  ```bash
  rmmod nome_do_modulo
  ```

- Ver informações sobre um módulo:
  ```bash
  modinfo nome_do_modulo
  ```

- Os módulos do kernel ficam em:
  ```
  /lib/modules/<versão>/
  ```

> 💡 Os módulos ficam armazenados em `/lib/modules/<versão_do_kernel>/` e são carregados automaticamente conforme o hardware ou o sistema exige.

Essa arquitetura modular é uma das grandes vantagens do Linux, pois permite adaptar o sistema a diferentes cenários — desde servidores enxutos até distribuições embarcadas ou sistemas com hardware específico.

---

## 💬 O que é o Shell?

O **shell** é um programa que serve como interface entre o usuário e o sistema operacional. Ele interpreta comandos digitados pelo usuário e os repassa ao kernel para execução. Em outras palavras, o shell é o “tradutor” entre você e o núcleo do sistema.

Existem dois tipos principais de shell:

- **Shell interativo**: quando você digita comandos diretamente no terminal.
- **Shell de script**: quando você escreve comandos em arquivos `.sh` para execução automatizada.

---

### 🐚 Tipos de Shell mais comuns

| Shell     | Caminho típico     | Características principais                                 |
|-----------|--------------------|-------------------------------------------------------------|
| `bash`    | `/bin/bash`        | O mais comum em distribuições Linux. Rico em recursos.     |
| `sh`      | `/bin/sh`          | Shell POSIX padrão. Simples e portátil.                    |
| `zsh`     | `/bin/zsh`         | Interativo, personalizável, usado com Oh My Zsh.           |
| `fish`    | `/usr/bin/fish`    | Focado em usabilidade e sugestões automáticas.             |
| `dash`    | `/bin/dash`        | Muito leve e rápido. Usado no boot em algumas distros.     |
| `ksh`     | `/bin/ksh`         | KornShell. Histórico e poderoso, usado em ambientes Unix.  |

Você pode descobrir qual shell está usando com:

```bash
echo $SHELL
```

E listar os shells disponíveis no sistema com:

```bash
cat /etc/shells
```

### 🧪 Exemplo de uso do shell

```bash
# Comando simples
ls -lh /etc

# Script básico
#!/bin/bash
echo "Olá, mundo!"
```

> 💡 O shell não é parte do kernel, mas é a principal ferramenta para interagir com ele — seja para executar comandos, automatizar tarefas ou administrar o sistema.

---

## 📖 Leitura complementar

- [Documentação oficial do kernel Linux](https://www.kernel.org/doc/)
- [Repositório oficial do código-fonte do kernel](https://github.com/torvalds/linux)
- `man 7 proc` – Manual sobre o sistema de arquivos /proc
- `man uname` – Exibe informações do sistema

---

## 📬 Contribuições

Se este projeto te ajudou ou inspirou, considere deixar uma estrela ⭐ no repositório!

Sinta-se à vontade para abrir *issues* com sugestões, correções ou dúvidas. Este repositório é um espaço voltado à **evolução constante** e à consolidação de boas práticas no uso do Linux como plataforma de infraestrutura.

---

## 🔗 Navegação Rápida

➡️ [Avançar para: `02 - Distribuições Linux`](./2-distributions.pt-BR.md)    
🔙 [Voltar para introdução do capítulo](./README.pt-BR.md)

---

## 📫 Contato

Caso deseje entrar em contato para oportunidades ou dúvidas:

- 🌐 [https://javadeveloper.com.br/](https://javadeveloper.com.br/)  
- 💼 [LinkedIn](https://www.linkedin.com/in/antonio-javadeveloper/)  
- 📧 antonio@javadeveloper.com.br  

> Developed by [AntonioJavaDeveloper](https://github.com/AntonioJavaDeveloper)