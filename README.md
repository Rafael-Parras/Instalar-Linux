# 🐧 Guia de Instalação: Fedora 43 no VirtualBox

![Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen)
![OS](https://img.shields.io/badge/OS-Fedora%2043-blue)
![VirtualBox](https://img.shields.io/badge/VirtualBox-7.0-orange)

Este repositório contém a documentação completa para a instalação do Fedora 43 em ambiente virtualizado utilizando o Oracle VM VirtualBox. Ideal para estudantes e desenvolvedores que buscam um ambiente de testes seguro.

---

## 🛠️ Pré-requisitos

Antes de iniciar, certifique-se de ter instalado:
* VirtualBox (Versão 7.0 ou superior recomendada)
* Imagem ISO do Fedora Workstation 43
* Pelo menos **25GB** de espaço em disco e **4GB** de RAM disponíveis

---

## 🚀 Manual de Instalação

### 1. Criação da Máquina Virtual (VM)
1. Abra o VirtualBox e clique em **Novo**
2. Defina o nome da VM como `Fedora 43`
3. Tipo: **Linux**
4. Versão: **Fedora (64-bit)**
5. Selecione a ISO do Fedora

> **[PRINT 1]**
> Tela de criação da VM (mostrar nome, tipo, versão e ISO selecionada)  
> ![Criação da VM](assets/print1.png)

---

### 2. Configuração de Hardware
1. Defina pelo menos:
   - **2048 MB de RAM** (recomendado 4096 MB)
   - **2 CPUs**

> **[PRINT 2]**
> Tela de configuração de memória e processador  
> ![Hardware](assets/print2.png)

---

### 3. Configurações de Armazenamento
1. Vá em `Configurações > Armazenamento`
2. Verifique se a ISO do Fedora está montada no CD/DVD

> **[PRINT 3]**
> Tela de armazenamento mostrando a ISO conectada  
> ![Armazenamento](assets/print3.png)

---

### 4. Processo de Instalação do Fedora
1. Clique em **Iniciar**
2. Selecione **Install Fedora**
3. Escolha:
   - Idioma
   - Fuso horário
   - Disco (pode usar automático)
   - Criação de usuário

> **[PRINT 4]**
> Tela do instalador (usuário ou particionamento)  
> ![Instalação](assets/print4.png)

---

### 5. Pós-Instalação: Guest Additions
Para melhorar desempenho e tela cheia:

1. No menu da VM:
   `Dispositivos > Inserir imagem de CD dos Adicionais de Convidado`
2. Execute no terminal:

```bash
sudo dnf install -y gcc kernel-devel kernel-headers dkms make bzip2
sudo mkdir /media/cdrom
sudo mount /dev/cdrom /media/cdrom
cd /media/cdrom
sudo ./VBoxLinuxAdditions.run
