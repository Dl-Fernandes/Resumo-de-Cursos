# 🐙 Resumo de Git & GitHub

<p align="center">
  <img src="https://shields.io" alt="Git">
  <img src="https://shields.io" alt="GitHub">
</p>

Este guia centraliza os conceitos teóricos, links de instalação e os comandos essenciais do Git praticados durante o bootcamp da **DIO**. Ele serve como material de consulta rápida para o dia a dia de desenvolvimento.

---

## 💾 Instalação e Downloads

Para utilizar o Git no seu computador, faça o download da versão oficial adequada para o seu sistema operacional:

* 📥 **Site Oficial do Git:** [git-scm.com](https://git-scm.com)
* 🪟 **Download Direto para Windows:** [Git for Windows (inclui Git Bash)](https://git-scm.comdownload/win)
* 🐧 **Instalação no Linux (Ubuntu/Debian):** `sudo apt update && sudo apt install git`

---

## 🛠️ Guia de Comandos Básicos

### 1️⃣ Configuração Inicial
Executado apenas uma vez após instalar o Git para identificar a autoria dos seus commits:
```bash
# Configurar seu nome de usuário
git config --global user.name "Seu Nome"

# Configurar seu e-mail (use o mesmo e-mail cadastrado no GitHub)
git config --global user.email "seu-email@provedor.com"
```

### 2️⃣ Iniciando e Clonando Repositórios
```bash
# Iniciar um repositório Git local em uma pasta vazia
git init

# Clonar um repositório remoto existente para a sua máquina
git clone https://github.com
```

### 3️⃣ O Fluxo Principal de Trabalho
```bash
# Verificar o estado atual dos arquivos (modificados, não rastreados, etc.)
git status

# Adicionar um arquivo específico para a área de preparação (Staging Area)
git add nome-do-arquivo.txt

# Adicionar TODOS os arquivos modificados de uma vez só
git add .

# Gravar as alterações salvas na Staging Area no histórico local
git commit -m "Explique aqui o que você fez de forma direta"
```

### 4️⃣ Sincronização com o GitHub (Servidor Remoto)
```bash
# Vincular o seu repositório local a um repositório remoto no GitHub
git remote add origin https://github.com/Dl-Fernandes/Resumo-de-Cursos.git

# Enviar as alterações locais da branch 'main' para o GitHub (primeira vez)
git push -u origin main

# Enviar alterações nas vezes seguintes (após o primeiro push configurado)
git push

# Atualizar seu repositório local com as alterações que estão no GitHub
git pull
```

---

## 🔗 Atalho de Navegação
* ⬅️ [Voltar para o Menu Principal de Cursos](../README.md)