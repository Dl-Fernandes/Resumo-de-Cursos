# 🐳 Docker

Comandos e conceitos básicos aprendidos durante os estudos de Docker.

---

## 🛠️ 1. Instalação do Docker

Comandos utilizados para instalar o Docker em distribuições Linux.

* `curl -fsSL https://get.docker.com -o get-docker.sh` → Baixa o script oficial de instalação do Docker.
* `sh get-docker.sh` → Executa o script de instalação do Docker.

---

## 🔍 2. Verificação da Instalação

Comandos utilizados para verificar se o Docker foi instalado corretamente.

* `docker version` → Exibe a versão do cliente e do servidor Docker.
* `systemctl status docker` → Verifica se o serviço Docker está em execução.

---

## 📥 3. Gerenciamento de Imagens

Comandos utilizados para baixar e listar imagens Docker.

* `docker pull [imagem]` → Baixa uma imagem do Docker Hub.
* `docker images` → Lista todas as imagens armazenadas localmente.

### Exemplos

* `docker pull nginx` → Baixa a imagem do Nginx.
* `docker pull ubuntu` → Baixa a imagem do Ubuntu.
* `docker pull mysql` → Baixa a imagem do MySQL.

---

## 📦 4. Gerenciamento de Containers

Comandos utilizados para criar, executar, acessar e interromper containers.

* `docker run [imagem]` → Cria e executa um container a partir de uma imagem.
* `docker run [imagem] sleep [segundos]` → Mantém o container em execução durante o tempo especificado.
* `docker run -it [imagem]` → Executa um container em modo interativo, permitindo utilizar o terminal interno do container.
* `docker ps` → Exibe apenas os containers em execução.
* `docker ps -a` → Exibe todos os containers, inclusive os que já foram encerrados.
* `docker stop [container]` → Interrompe a execução de um container.

### Exemplos

* `docker run ubuntu` → Executa um container baseado na imagem Ubuntu.
* `docker run ubuntu sleep 10` → Mantém o container ativo por 10 segundos.
* `docker run ubuntu sleep 60` → Mantém o container ativo por 1 minuto.
* `docker run -it ubuntu` → Inicia um terminal interativo dentro de um container Ubuntu.
* `docker ps` → Exibe os containers em execução.
* `docker ps -a` → Exibe todos os containers criados.
* `docker stop hopeful_morse` → Interrompe o container chamado `hopeful_morse`.

### Conceitos Importantes

* `-i` → Mantém a entrada padrão (STDIN) aberta.
* `-t` → Cria um terminal virtual (TTY).
* `-it` → Combina os dois parâmetros, permitindo interação direta com o container.
* `sleep` → Comando utilizado para manter o container ativo por um período específico.


---

## 📚 Conceitos Importantes

### Imagem (Image)

Uma imagem é um modelo pronto contendo sistema operacional, bibliotecas, dependências e aplicações necessárias para executar um serviço.

### Container

Um container é uma instância em execução de uma imagem Docker.

### Docker Hub

Repositório online utilizado para armazenar e compartilhar imagens Docker.

---

## 📝 Resumo Rápido

* `docker pull nginx` → Baixa uma imagem.
* `docker images` → Lista imagens.
* `docker run nginx` → Executa um container.
* `docker ps` → Lista containers em execução.
* `docker ps -a` → Lista todos os containers.
* `docker version` → Exibe a versão do Docker.
* `systemctl status docker` → Verifica o status do serviço.
