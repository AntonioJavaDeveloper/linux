# 🐧 Linux como Plataforma de Infraestrutura: Fundamentos, Automação e Boas Práticas

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Stars](https://img.shields.io/github/stars/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/stargazers)
[![Forks](https://img.shields.io/github/forks/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/network/members)

Este repositório apresenta uma coleção de soluções, práticas e conceitos essenciais para a construção, administração e automação de ambientes baseados em **Linux**. Cada branch aborda um aspecto específico do sistema operacional — como permissões, processos, rede, segurança e integração com ferramentas de automação, entre outros.

Os exemplos práticos são organizados de forma modular e, quando aplicável, implementados em **Java**, demonstrando como linguagens de propósito geral podem interagir com o sistema operacional para tarefas como manipulação de arquivos, execução de comandos e monitoramento de recursos.

Para facilitar a reprodução dos cenários, os capítulos incluem ambientes configuráveis com **Vagrant** — permitindo que qualquer pessoa execute os exemplos de forma isolada e controlada, sem depender da configuração do sistema local. No entanto, o uso do Vagrant é opcional: o foco está nos conceitos e práticas que podem ser aplicados em qualquer distribuição Linux.

O objetivo é oferecer uma referência sólida e reutilizável para profissionais que atuam com infraestrutura, DevOps ou desenvolvimento backend, com foco em clareza, eficiência e boas práticas.


---

## ⚙️ Requisitos

Para executar os ambientes de exemplo fornecidos neste repositório, é necessário ter as seguintes ferramentas instaladas na máquina local:

- [**Oracle VirtualBox**](https://www.virtualbox.org/) – Hypervisor gratuito utilizado como provedor padrão para as máquinas virtuais.
- [**Vagrant**](https://www.vagrantup.com/) – Ferramenta de automação para provisionamento e gerenciamento de ambientes de desenvolvimento.

> 💡 O uso dessas ferramentas é recomendado apenas para quem deseja executar os exemplos localmente. O conteúdo conceitual e os trechos de código podem ser compreendidos independentemente da execução prática.

---

## 🗂️ Organização dos Capítulos

Este repositório está estruturado em **capítulos temáticos**, cada um abordando um aspecto específico do sistema operacional Linux. Para manter o conteúdo modular e versionável, **cada capítulo está localizado em uma branch separada**.

### 📌 Estrutura por Branches

- A branch `main` funciona como índice central do projeto. Ela contém o `README.pt-BR.md` e o `README.md` com a visão geral, os requisitos e a navegação entre os capítulos.
- Cada capítulo possui sua própria branch, nomeada com um prefixo numérico e um identificador em inglês (ex: `01-fhs`, `02-boot-process`, `03-systemd`).
- Dentro de cada branch, podem existir múltiplos arquivos `README.md` para cobrir diferentes seções ou subtemas do capítulo.
- Todos os arquivos de documentação são disponibilizados em **português (`README.pt-BR.md`)** e **inglês (`README.md`)**.

### 🧭 Navegação entre Capítulos

Ao final do `README.pt-BR.md` da branch `main`, você encontrará a seção **📚 Catálogo de Capítulos**, que reúne todos os temas abordados neste repositório. Cada linha da tabela contém o título do capítulo e um link direto para o conteúdo correspondente, facilitando a navegação entre os assuntos.

Exemplo de estrutura de navegação:

| Capítulo                                          | Link para o conteúdo em português                                                                                      |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| 00 - Fundamentos do Linux: Kernel e Distribuições | [📘 `00-linux-fundamentals`](https://github.com/AntonioJavaDeveloper/linux/blob/00-linux-fundamentals/README.pt-BR.md) |
| 01 - Estrutura de Diretórios do Linux             | [📘 `01-fhs`](https://github.com/AntonioJavaDeveloper/linux/blob/01-fhs/README.pt-BR.md)                               |
| 02 - Inicialização do Sistema (Boot)              | [📘 `02-boot-process`](https://github.com/AntonioJavaDeveloper/linux/blob/02-boot-process/README.pt-BR.md)             |



> 💡 A tabela acima apresenta um resumo dos capítulos disponíveis. Para acessar qualquer capítulo, basta clicar no link correspondente — você será direcionado diretamente para o conteúdo da branch específica no GitHub, sem necessidade de clonar ou utilizar comandos Git.

> A listagem completa com todos os capítulos pode ser consultada na seção **📚 Catálogo de Capítulos**, localizada ao final deste arquivo.

---

## 📚 Catálogo de Capítulos

| Capítulo                                          | Link para o conteúdo em português                                                                                      |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| 00 - Fundamentos do Linux: Kernel e Distribuições | [📘 `00-linux-fundamentals`](https://github.com/AntonioJavaDeveloper/linux/blob/00-linux-fundamentals/README.pt-BR.md) |
| 01 - Estrutura de Diretórios do Linux             | [📘 `01-fhs`](https://github.com/AntonioJavaDeveloper/linux/blob/01-fhs/README.pt-BR.md)                               |
| 02 - Inicialização do Sistema (Boot)              | [📘 `02-boot-process`](https://github.com/AntonioJavaDeveloper/linux/blob/02-boot-process/README.pt-BR.md)             |
| 03 - Gerenciamento de Serviços com systemd        | [📘 `03-systemd`](https://github.com/AntonioJavaDeveloper/linux/blob/03-systemd/README.pt-BR.md)                       |

---

## 📬 Contribuições

Se este projeto te ajudou ou inspirou, considere deixar uma estrela ⭐ no repositório!

Sinta-se à vontade para abrir *issues* com sugestões, correções ou dúvidas. Este repositório é um espaço voltado à **evolução constante** e à consolidação de boas práticas no uso do Linux como plataforma de infraestrutura.

---

## 🔗 Navegação Rápida

➡️ [Avançar para `00 - Fundamentos do Linux: Kernel e Distribuições`](https://github.com/AntonioJavaDeveloper/linux/blob/00-linux-fundamentals/README.pt-BR.md)

---

## 📫 Contato

Caso deseje entrar em contato para oportunidades ou dúvidas:

- 🌐 [https://javadeveloper.com.br/](https://javadeveloper.com.br/)
- 💼 [LinkedIn](https://www.linkedin.com/in/antonio-javadeveloper/)
- 📧 antonio@javadeveloper.com.br

> Developed by [AntonioJavaDeveloper](https://github.com/AntonioJavaDeveloper)
