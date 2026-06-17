# 🐧 Resumo de Comandos Linux

<p align="center">
  <img src="https://shields.io" alt="Linux">
  <img src="https://shields.io" alt="Terminal">
</p>

Guia prático e documentação técnica com os comandos essenciais do sistema operacional Linux, consolidados durante o bootcamp **Linux Experience** na **DIO**.

---

## 🧭 1. Navegação, Localização e Terminal

Comandos fundamentais para entender o posicionamento na árvore de diretórios e movimentação no sistema.

* `pwd` &rarr; Mostra o caminho absoluto da pasta atual (Print Working Directory).
* `cd /` &rarr; Altera o foco direto para a pasta raiz do sistema operacional.
* `cd ~` ou apenas `cd` &rarr; Retorna direto para a pasta pessoal do usuário atual (Home).
* `cd ..` &rarr; Volta um nível para a pasta anterior (diretório pai).
* `cd [pasta]` &rarr; Entra no diretório especificado.
* `clear` ou `Ctrl + L` &rarr; Limpa o histórico visual da tela do terminal.
* `TAB` (Pressionar 2 vezes) &rarr; Autocompleta comandos ou lista caminhos disponíveis (Ex: `cd /var/` + `TAB` `TAB`).

---

## 🔍 2. Listagem e Filtros Avançados (`ls`)

Comandos utilizados para listar o conteúdo de diretórios utilizando parâmetros de refinamento e expressões regulares (*wildcards*).

* `ls` &rarr; Listagem simples. (Diretórios aparecem em azul, arquivos comuns em branco/verde).
* `ls -a` &rarr; Lista todos os arquivos, incluindo os arquivos ocultos (iniciados com ponto, ex: `.bashrc`).
* `ls -l` &rarr; Exibe a listagem detalhada (permissões, quantidade de links, proprietário, grupo, tamanho e data).
* `ls -lh` &rarr; Igual ao `-l`, mas exibe o tamanho dos arquivos em formato legível para humanos (KB, MB, GB).
* `ls | more` ou `ls | less` &rarr; Pagina a listagem de arquivos na tela. Use `Espaço` para rolar e `Q` para sair.
* `ls arquivo*` &rarr; Lista arquivos que iniciam exatamente com o termo "arquivo".
* `ls arquivo[1-3]*` &rarr; Lista arquivos que começam com o nome e possuem números no intervalo de 1 a 3.
* `ls arquivo[^1,3]*` &rarr; Lista os arquivos, exceto os terminados com os números 1 ou 3.

---

## 📂 3. Busca de Arquivos e Conteúdo (`find` e `grep`)

* `find . -name "arquivo"` &rarr; Procura por arquivos com o nome exato a partir do diretório atual (`.`).
* `cat /diretorio/arquivo` &rarr; Exibe todo o conteúdo de um arquivo de texto diretamente no terminal.
* `grep "termo" arquivo` &rarr; Filtra e exibe linhas que contenham uma palavra específica dentro do arquivo de texto.

---

## 🛠️ 4. Manipulação de Arquivos e Pastas

* `touch arquivo.txt` &rarr; Cria um arquivo vazio ou atualiza a data de modificação de um arquivo existente.
* `mkdir pasta` &rarr; Cria um novo diretório.
* `rmdir pasta` &rarr; Remove uma pasta, desde que ela esteja **completamente vazia**.
* `rm arquivo` &rarr; Exclui um arquivo permanentemente.
* `rm -rf pasta` &rarr; **Cuidado Extremo:** Força (`-f`) a exclusão recursiva (`-r`) de um diretório e de todo o seu conteúdo.

### 📦 Cópia e Movimentação Avançada (`cp` / `mv`)
A estrutura dos comandos segue o padrão: `comando [origem] [destino]`.

* **Parâmetros úteis:**
  * `-r` &rarr; Copia diretórios de forma recursiva.
  * `-i` &rarr; Modo interativo; pergunta antes de sobrescrever um arquivo existente.
  * `-v` &rarr; Modo *verbose*; exibe detalhadamente cada passo executado na tela.

* **Exemplos de uso prático:**
  * `cp /home/daniel/banco.mdf /mnt/disco2` &rarr; Copia um arquivo específico para outro ponto de montagem.
  * `cp /home/daniel/*.txt /mnt/disco2` &rarr; O caractere `*` serve de filtro para copiar todos os arquivos `.txt`.
  * `cp ./a* /mnt/disco2` &rarr; O `.` indica a pasta atual. Copia todos os arquivos que começam com a letra "a".
  * `cp /home/daniel/* /mnt/disco2 -i` &rarr; Copia todos os arquivos da pasta (ignora subpastas sem o `-r`) e pede confirmação antes de sobrescrever.
  * `mv banco.mdf banco_de_dados.mdf` &rarr; Renomeia o arquivo original no mesmo diretório.

---

## 🔒 5. Gerenciamento de Usuários, Grupos e Permissões

Administração de contas e controle de acessos no sistema. O superusuário administrador é conhecido como **Root**.

### Identificação e Grupos
* `cat /etc/passwd` &rarr; Arquivo do sistema que lista todas as contas de usuários.
* `cat /etc/group` &rarr; Arquivo do sistema que lista todos os grupos e seus respectivos membros.
* `groupadd [nome_do_grupo]` &rarr; Cria um novo grupo no sistema.
* `groupdel [nome_do_grupo]` &rarr; Remove um grupo existente.

### Criação e Modificação de Usuários
* `su` &rarr; Alterna para o usuário root (exige a senha do root).
* `su - usuario` &rarr; Alterna para a conta de outro usuário comum carregando suas variáveis de ambiente.
* `sudo [comando]` &rarr; Executa um comando isolado com privilégios administrativos de root.
* `useradd -m -c "Nome Completo" -s /bin/bash usuario` &rarr; Cria um usuário definindo pasta home (`-m`), comentário/nome (`-c`) e o shell padrão (`-s`).
* `useradd usuario -c "Comentario" -m -s /bin/bash -p $(openssl passwd -6 senha)` &rarr; Cria um usuário definindo a senha criptografada via linha de comando.
* `usermod -aG sudo usuario` &rarr; Adiciona (`-a`) o usuário ao grupo administrativo (`G`) sudo sem removê-lo dos grupos atuais.
* `usermod -G adm,sudo usuario` &rarr; Define e substitui as permissões do usuário adicionando-o aos grupos listados.
* `usermod -G [grupo] [usuario]` &rarr; Vincula um usuário a um grupo específico.
* `userdel -rf usuario` &rarr; Remove permanentemente o usuário do sistema, forçando a operação (`-f`) e deletando sua pasta home (`-r`).
* `passwd usuario` &rarr; Altera ou define a senha de acesso do usuário.
* `passwd -e usuario` &rarr; Força a expiração (`-e`) da senha atual, obrigando o usuário a alterá-la no próximo logon.

### Alteração de Propriedades (Dono/Grupo)
* `chown [usuario]:[grupo] /[diretorio]` &rarr; Altera simultaneamente o usuário proprietário e o grupo dono de um diretório ou arquivo.

---

## 📝 6. Editores de Texto via Terminal

### 💻 Editor Nano
* `Ctrl + O` &rarr; Grava/Salva as alterações feitas no arquivo.
* `Ctrl + X` &rarr; Sai do editor de texto.
* `Ctrl + K` &rarr; Recorta a linha de texto atual.
* `Ctrl + U` &rarr; Cola a linha previamente recortada.

### 🎛️ Editor Vi / Vim
Funciona de maneira multimodal. Os modos principais são **Comando** e **Inserção**.
* `i` &rarr; Entra no modo de edição (Inserção).
* `Esc` &rarr; Sai do modo de edição e retorna ao modo de comando básico.
* `:wq` &rarr; Salva as alterações (*write*) e fecha o arquivo (*quit*).
* `:q!` &rarr; Força a saída do editor sem salvar nenhuma das alterações feitas.

---

## ⏱️ 7. Histórico e Variáveis de Ambiente

* `history` &rarr; Exibe a lista cronológica de comandos executados no terminal.
* `!!` &rarr; Executa novamente o último comando rodado.
* `!grep` &rarr; Executa o último comando do histórico iniciado com o termo "grep".
* `history | grep "termo"` &rarr; Filtra a lista do histórico exibindo apenas ocorrências que correspondam ao termo buscado.
* `set +o history` &rarr; Desativa temporariamente o registro de novos comandos no histórico do terminal.
* `set -o history` &rarr; Reativa a gravação padrão de novos comandos no histórico.
* `export VARIAVEL="valor"` &rarr; Cria ou altera uma variável de ambiente (por convenção, escritas em MAIÚSCULO).

---

## 📜 8. Scripts e Execução de Automações (`.sh`)

Os arquivos de automação em lote devem seguir os pré-requisitos abaixo:

1. **Shebang Obrigatório:** A primeiríssima linha do arquivo deve indicar o interpretador correto:
   ```bash
   #!/bin/bash
   ```
2. **Permissão de Execução:** Conceder o privilégio de execução ao script:
   ```bash
   chmod +x script.sh
   ```
3. **Execução:** Rodar informando o diretório relativo local:
   ```bash
   ./script.sh
   ```

---

## 📦 9. Gerenciamento de Pacotes (`apt`)

Comandos utilizados na distribuição Ubuntu/Debian para instalar e remover programas.

* `apt update` &rarr; Atualiza os índices de pacotes das listas de repositórios.
* `apt upgrade` &rarr; Atualiza efetivamente o sistema operacional aplicando as novas versões dos programas.
* `apt list --installed` &rarr; Lista todos os pacotes e softwares atualmente instalados na máquina.
* `apt list --upgradeable` &rarr; Exibe quais programas instalados possuem atualizações prontas para baixar.
* `apt search [programa]` &rarr; Procura nos repositórios se o software buscado está disponível para instalação.
* `apt install [programa]` &rarr; Baixa e instala o programa selecionado.
* `apt remove [programa]` &rarr; Desinstala um pacote do sistema.
* `apt remove [programa] -y` &rarr; Desinstala o pacote aceitando automaticamente todas as confirmações de segurança (`-y`).
* `apt edit-sources` &rarr; Abre o arquivo de configuração para adicionar ou remover repositórios de terceiros fora do espelho oficial do Ubuntu.
* `unzip [arquivo.zip]` &rarr; Utilitário para extrair e descompactar arquivos comprimidos de formato `.zip`.

---

## 💾 10. Gerenciamento de Armazenamento e Discos

### 📊 Visualização de Discos
* `lsblk` &rarr; Lista de forma em árvore os blocos de armazenamento disponíveis (discos e partições).
* `fdisk -l` &rarr; Lista detalhadamente as partições e sistemas de arquivos existentes (Requer privilégios de `root`).

### 🔨 Adicionando Nova Partição com o `fdisk`
Ao rodar o comando para abrir o utilitário (Ex: `fdisk /dev/sdb`), siga o passo a passo utilizando o menu interativo:

1. `d` &rarr; Deleta uma partição antiga existente (se aplicável).
2. `n` &rarr; Inicializa a criação de uma nova partição.
3. `p` &rarr; Define a nova partição criada como **Primária**.
4. **Número da partição:** Escolha ou digite o número identificador.
5. **Primeiro setor:** Pressione `Enter` para aceitar o valor padrão do sistema.
6. **Último setor:** Pressione `Enter` para aceitar o tamanho padrão máximo do disco.
7. `w` &rarr; Grava (*write*) as alterações na tabela de partições e sai do utilitário `fdisk`.

### 🗏 Formatar Nova Partição
* `mkfs.ext4 /dev/sdb1` &rarr; Formata a partição especificada utilizando o sistema de arquivos padrão do Linux (`ext4`).

---

## ⚙️ 11. Gerenciamento de Processos

* `ps` &rarr; Visualiza os processos ativos que estão em execução pelo usuário atual.
* `ps -a` &rarr; Exibe os processos em execução de todos os usuários do sistema.
* `ps -u` &rarr; Apresenta o nome do usuário e o horário detalhado em que o processo foi iniciado.
* `ps -x` &rarr; Lista processos executados fora do console (geralmente serviços que rodam em segundo plano).
* `kill [PID]` &rarr; Finaliza um processo de maneira limpa através do seu número de ID (PID).
* `killall [nome_do_processo]` &rarr; Encerra de uma vez só todas as instâncias em execução baseando-se no nome do aplicativo.

---

## ❓ 12. Ajuda e Documentação Oficial

* `[comando] --help` &rarr; Exibe um resumo rápido da sintaxe de uso do comando selecionado.
* `man [comando]` &rarr; Abre o manual oficial completo do comando (Pressione `Q` para fechar a tela do manual).

---

## 🖥️ 13. Informações do Sistema e Hardware

* `cat /proc/cpuinfo` → Exibe o arquivo com informações detalhadas do processador.
* `lscpu` → Exibe informações resumidas sobre o processador.
* `cat /proc/meminfo` → Exibe o arquivo com informações detalhadas da memória.
* `free` → Exibe informações sobre memória física e memória virtual.
* `lshw` → Exibe informações detalhadas sobre o hardware do sistema.
* `lshw -short` → Exibe um resumo das informações de hardware.
* `uname` → Exibe o nome do kernel do sistema.
* `uname -r` → Exibe a versão do kernel.
* `uname -m` → Exibe a arquitetura do sistema.
* `arch` → Exibe a arquitetura do sistema.
* `lspci` → Exibe todos os dispositivos PCI conectados.
* `lsusb` → Exibe todos os dispositivos USB conectados.
* `du -h ~` → Exibe o espaço ocupado por arquivos e diretórios do usuário.
* `reboot` → Reinicia o sistema.
* `shutdown -r` → Reinicia o sistema.
* `shutdown -h now` → Desliga o sistema imediatamente.

## 🔗 Atalho de Navegação
* ⬅️ [Voltar para o Menu Principal de Cursos](../README.md)
