---

# 📁 Sistemas de Arquivos

O sistema operacional utiliza sistemas de arquivos para organizar, armazenar e gerenciar os dados em dispositivos de armazenamento, como HDDs e SSDs.

Antes que um disco possa ser utilizado para armazenar arquivos, ele precisa ser configurado e formatado com um sistema de arquivos compatível.

---

## ⚙️ Funções de um Sistema de Arquivos

O sistema de arquivos é responsável por:

- 💽 Configurar o dispositivo de armazenamento para leitura e gravação de dados;
- 📍 Controlar onde cada arquivo está armazenado;
- 📊 Gerenciar o espaço disponível no disco;
- 🔒 Controlar permissões de acesso;
- 🛡️ Ajudar a manter a integridade dos dados;
- 📂 Organizar os arquivos e diretórios.

Em resumo, o sistema de arquivos permite que o sistema operacional encontre, acesse e organize os arquivos de forma eficiente.

---

# 🗂️ Exemplos de Sistemas de Arquivos

## 🪟 NTFS (New Technology File System)

Sistema de arquivos utilizado principalmente pelo Windows.

Entre seus recursos estão:

- 🔒 Permissões de acesso;
- 🔐 Criptografia;
- 📁 Suporte a arquivos e volumes de grande capacidade;
- 🛡️ Recursos de segurança e integridade dos dados.

---

## 🐧 EXT4 (Fourth Extended Filesystem)

Sistema de arquivos muito utilizado em sistemas Linux.

Entre suas características estão:

- 📂 Organização eficiente dos arquivos;
- ⚡ Bom desempenho;
- 🔄 Compatibilidade com versões anteriores da família EXT;
- 💽 Suporte a grandes volumes de armazenamento.

---

# 💾 Armazenamento de Dados em Blocos

Os arquivos são armazenados em blocos no dispositivo de armazenamento.

Um único arquivo pode ocupar vários blocos diferentes no disco.

Esses blocos podem estar:

- 📍 Próximos uns dos outros;
- 🧩 Espalhados em diferentes áreas do disco.

Quando partes de um arquivo são armazenadas em diferentes locais, ocorre a **fragmentação**.

O sistema de arquivos mantém informações sobre a localização desses blocos para que o sistema operacional consiga encontrar e acessar o arquivo corretamente.

---

# 🧩 Fragmentação

A fragmentação ocorre quando partes de um arquivo são armazenadas em diferentes áreas do dispositivo de armazenamento.

Isso pode aumentar o tempo necessário para localizar e acessar os dados, principalmente em discos rígidos mecânicos (HDDs).

O sistema operacional pode utilizar ferramentas de desfragmentação para reorganizar os dados e melhorar a disposição dos arquivos no disco.

---

# 🏷️ Metadados

Metadados são informações que descrevem um arquivo, mas que não fazem parte do conteúdo principal do arquivo.

Eles ajudam o sistema operacional a organizar, gerenciar e proteger os dados.

Exemplos de metadados:

- 👤 Criador do arquivo;
- 📅 Data de criação;
- 🕒 Data da última modificação;
- 🔒 Permissões de acesso;
- 📄 Tipo do arquivo;
- 📏 Tamanho do arquivo;
- 📍 Localização do arquivo.

---

# 📄 Extensões de Arquivos

A extensão de um arquivo geralmente indica seu tipo e ajuda o sistema operacional a identificar qual programa pode ser utilizado para abri-lo.

Exemplos:

| Extensão | Tipo de Arquivo |
|----------|------------------|
| `.txt` | Arquivo de texto |
| `.jpg` | Imagem |
| `.png` | Imagem |
| `.mp3` | Áudio |
| `.mp4` | Vídeo |
| `.pdf` | Documento |
| `.docx` | Documento de texto |
| `.exe` | Programa executável |

A extensão normalmente aparece no final do nome do arquivo.

Por exemplo:

```text
documento.txt
foto.jpg
video.mp4
programa.exe
```

---

# 📌 Resumo

O sistema de arquivos é responsável por organizar e gerenciar os dados armazenados em um dispositivo.

Ele controla:

- 💽 Como o disco é configurado;
- 📂 Onde os arquivos são armazenados;
- 📊 Quanto espaço está disponível;
- 🏷️ Os metadados dos arquivos;
- 🔒 As permissões de acesso;
- 📄 Os tipos de arquivos.

Entre os sistemas de arquivos estudados estão o **NTFS**, utilizado principalmente pelo Windows, e o **EXT4**, muito utilizado em sistemas Linux.

Compreender os sistemas de arquivos é fundamental para o trabalho de suporte técnico, pois muitas tarefas envolvem formatação de discos, gerenciamento de armazenamento, permissões e recuperação de arquivos.
