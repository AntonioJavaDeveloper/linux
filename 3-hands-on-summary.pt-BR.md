# 🧪 03 - Laboratório Prático: Kernel e Distribuições em Ação

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Stars](https://img.shields.io/github/stars/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/stargazers)
[![Forks](https://img.shields.io/github/forks/AntonioJavaDeveloper/linux?style=social)](https://github.com/AntonioJavaDeveloper/linux/network/members)

---

## 🧭 Navegação

📂 [`README principal do repositório`](https://github.com/AntonioJavaDeveloper/linux/blob/main/README.pt-BR.md)  
└── 📁 [`Introdução do capítulo`](./README.pt-BR.md)  
&emsp;&emsp;├── [`01 - Kernel do Linux`](./1-kernel.pt-BR.md)  
&emsp;&emsp;├── [`02 - Distribuições Linux`](./2-distributions.pt-BR.md)    
&emsp;&emsp;├── [`03 - Laboratório Prático: Kernel e Distribuições em Ação`](./3-hands-on-summary.pt-BR.md) ← **você está aqui**  

---

## 📚 Introdução

Este laboratório prático tem como finalidade demonstrar, de forma objetiva, a aplicação dos conceitos abordados nesse capítulo — com foco na identificação do kernel, manipulação de módulos e reconhecimento de distribuições Linux em ambientes distintos.

Para isso, serão utilizados dois ambientes virtuais provisionados com Vagrant:

- 🐧 Ubuntu (base Debian)
- 🐮 Rocky Linux (base Red Hat)

Os arquivos de configuração necessários já estão disponíveis no diretório `vagrant`, localizado na raiz do repositório. Não é necessário escrever os códigos manualmente — basta executar os comandos indicados para inicializar os ambientes e realizar os testes propostos.

```
📁 vagrant/
└── 📁 ubuntu/
    └── Vagrantfile
└── 📁 rocky/
    └── Vagrantfile
```

Você poderá executar comandos reais para:

- Verificar a versão do kernel
- Explorar módulos do kernel
- Identificar a distribuição em uso
- Testar comandos básicos com `apt` e `dnf`

---

## 🚀 Subindo os ambientes com Vagrant

Crie dois arquivos Vagrantfile, cada um em seu respectivo diretório:

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

Para iniciar os ambientes, acesse o diretório correspondente e execute os comandos abaixo:

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

## 📂 Verificando o Kernel

| Comando                     | Descrição                          | Esperado (exemplo)          |
|-----------------------------|------------------------------------|-----------------------------|
| `uname -r`                  | Versão do kernel                   | `5.15.0-105-generic`        |
| `ls /boot`                  | Ver arquivos do kernel             | `vmlinuz`, `initrd.img`     |
| `cat /proc/version`         | Informações detalhadas do kernel   | Kernel + compilador usado   |

---

## 🧩 Explorando Módulos

| Comando                     | Descrição                          |
|-----------------------------|------------------------------------|
| `lsmod`                     | Lista módulos carregados           |
| `modinfo <módulo>`          | Exibe informações de um módulo     |
| `modprobe <módulo>`         | Carrega um módulo manualmente      |
| `rmmod <módulo>`            | Remove um módulo                   |

---

## 🧠 Identificando a Distribuição

| Comando                     | Ubuntu                            | Rocky Linux                      |
|-----------------------------|------------------------------------|----------------------------------|
| `cat /etc/os-release`       | `Ubuntu 20.04`                     | `Rocky Linux 9`                  |
| `hostnamectl`               | Mostra nome, kernel e sistema      | Mostra nome, kernel e sistema    |

---

## 📦 Testando o gerenciador de pacotes

| Ação                        | Ubuntu (APT)                      | Rocky (DNF)                      |
|-----------------------------|-----------------------------------|----------------------------------|
| Atualizar lista de pacotes  | `sudo apt update`                | `sudo dnf check-update`         |
| Instalar pacote `curl`      | `sudo apt install htop`          | `sudo dnf install htop`         |
| Remover pacote `curl`       | `sudo apt remove htop`           | `sudo dnf remove htop`          |

> ⚠️ Este laboratório não substitui os capítulos específicos sobre gerenciamento de pacotes. Aqui o foco é apenas validar o ambiente e reforçar os conceitos de kernel e distribuição.

---

## 🛑 Encerrando o ambiente

Após concluir os testes propostos neste laboratório, recomenda-se remover os ambientes provisionados para liberar recursos do sistema. Abaixo estão os comandos para remoção das máquinas virtuais e, opcionalmente, dos boxes utilizados.

### 🧹 Removendo as máquinas virtuais

Em cada diretório (vagrant/ubuntu e vagrant/rocky), execute o comando abaixo para remover as máquinas virtuais:

```bash
vagrant destroy -f
```

> 💡 O comando `destroy` remove a máquina virtual criada, mas mantém o box base armazenado localmente. Isso permite que o ambiente seja recriado rapidamente no futuro, sem novo download.

---

### 🗑️ Removendo boxes baixados

Caso deseje liberar espaço em disco e não pretenda reutilizar os boxes:

```bash
# Lista todos os boxes instalados
vagrant box list

# Remove os boxes utilizados neste laboratório
vagrant box remove bento/ubuntu-22.04
vagrant box remove generic/rocky9
```

> ⚠️ A remoção dos boxes implica que, ao executar `vagrant up` novamente, os arquivos serão baixados do zero.

---

## 📖 Leitura complementar

- [Documentação do Vagrant](https://developer.hashicorp.com/vagrant/docs)
- `man uname`, `man modprobe`, `man os-release`

---

## 📬 Contribuições

Se este projeto te ajudou ou inspirou, considere deixar uma estrela ⭐ no repositório!

Sinta-se à vontade para abrir *issues* com sugestões, correções ou dúvidas. Este repositório é um espaço voltado à **evolução constante** e à consolidação de boas práticas no uso do Linux como plataforma de infraestrutura.

---

## 🔗 Navegação Rápida

➡️ [Avançar para o capítulo: `01 - Estrutura de Diretórios do Linux`](https://github.com/AntonioJavaDeveloper/linux/blob/01-fhs/README.pt-BR.md)  
🔙 [Voltar para: `02 - Distribuições Linux`](./2-distributions.pt-BR.md)

---

## 📫 Contato

Caso deseje entrar em contato para oportunidades ou dúvidas:

- 🌐 [https://javadeveloper.com.br/](https://javadeveloper.com.br/)
- 💼 [LinkedIn](https://www.linkedin.com/in/antonio-javadeveloper/)
- 📧 antonio@javadeveloper.com.br

> Developed by [AntonioJavaDeveloper](https://github.com/AntonioJavaDeveloper)

