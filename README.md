# 🐧 Guia de Instalação: Linux no VirtualBox

![Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen)
![OS](https://img.shields.io/badge/OS-Ubuntu%2024.04-orange)
![VirtualBox](https://img.shields.io/badge/VirtualBox-7.0-blue)

Este repositório contém a documentação completa para a instalação de uma distribuição Linux em ambiente virtualizado utilizando o Oracle VM VirtualBox. Ideal para estudantes e desenvolvedores que buscam um ambiente de testes seguro.

---

## 🛠️ Pré-requisitos

Antes de iniciar, certifique-se de ter instalado:
* [VirtualBox](https://www.virtualbox.org/) (Versão 7.0 ou superior recomendada).
* Imagem ISO da distribuição (Ex: [Ubuntu Desktop](https://ubuntu.com/download/desktop)).
* Pelo menos **25GB** de espaço em disco e **4GB** de RAM disponíveis.

---

## 🚀 Manual de Instalação

### 1. Criação da Máquina Virtual (VM)
1. Abra o VirtualBox e clique em **Novo**.
2. Defina o nome da VM, a pasta de destino e selecione a ISO baixada.
3. No hardware, reserve ao menos **2048 MB** de RAM e **2 CPUs**.

> **[INSERIR AQUI: Print da tela de criação da VM no VirtualBox]**
> *Legenda: Configuração inicial de nome e recursos da máquina.*

### 2. Configurações de Armazenamento
Para garantir que a VM inicie pelo "instalador":
1. Vá em `Configurações > Armazenamento`.
2. Verifique se o arquivo `.iso` está montado na unidade de CD/DVD.

> **[INSERIR AQUI: Print da aba de armazenamento com a ISO selecionada]**

### 3. O Processo de Instalação do OS
1. Clique em **Iniciar**.
2. Escolha o idioma e o layout do teclado.
3. Selecione **Instalação Normal** e a opção **"Apagar disco e instalar o Ubuntu"** (Lembrando que isso afeta apenas o disco virtual).
4. Defina seu fuso horário e crie seu usuário.

> **[INSERIR AQUI: Print da tela de particionamento ou criação de usuário]**

### 4. Pós-Instalação: Guest Additions
Para habilitar tela cheia e área de transferência compartilhada:
1. No menu superior da janela da VM, vá em `Dispositivos > Inserir Imagem de CD dos Adicionais de Convidado`.
2. Siga as instruções no terminal e reinicie a máquina.

---

## 🖥️ Resultado Final
Após o reboot, o sistema estará pronto para uso.

> **[INSERIR AQUI: Print do Desktop do Linux rodando em tela cheia no VirtualBox]**

---

## 🛠️ Comandos Úteis (Pós-Instalação)
Abra o terminal (`Ctrl+Alt+T`) e execute:

```bash
# Atualizar a lista de repositórios
sudo apt update

# Instalar as atualizações do sistema
sudo apt upgrade -y


---

### 💡 Dicas para os seus Prints:
1.  **Recorte bem:** Não tire print da sua área de trabalho inteira. Foque apenas na janela do VirtualBox ou na caixa de diálogo específica. Isso deixa o documento muito mais limpo.
2.  **Organização de arquivos:** No seu repositório do GitHub, crie uma pasta chamada `/assets` ou `/img` e salve as imagens lá. No código do README, o caminho ficará assim: `![Legenda](assets/print01.png)`.
3.  **Witty Tip:** Se quiser dar um toque extra, inclua um print do comando `neofetch` (ou `screenfetch`) rodando no terminal ao final. É o "batismo" oficial de qualquer instalação Linux bem-sucedida!
