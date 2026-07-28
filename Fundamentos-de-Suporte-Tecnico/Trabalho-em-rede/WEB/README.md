# 🌐 A Web e os Endereços da Internet

A **Web (World Wide Web)** é uma das principais formas de acessar informações e serviços disponíveis na Internet.

Por meio da Web, podemos acessar:

* 🌐 Sites;
* 📄 Páginas web;
* 🖼️ Imagens;
* 🎥 Vídeos;
* 🎵 Áudios;
* 📝 Documentos;
* 🖥️ Aplicações web.

---

# 🌐 O que são Páginas Web?

As páginas web são documentos acessados por meio de navegadores.

Elas são geralmente construídas utilizando **HTML (HyperText Markup Language)**.

O HTML permite estruturar conteúdos como:

* 📝 Textos;
* 🖼️ Imagens;
* 🔗 Links;
* 🎥 Vídeos;
* 🎵 Áudios;
* 📋 Formulários.

Uma página web pode ser representada assim:

```text
💻 Usuário
      ↓
🌐 Navegador
      ↓
🔗 URL
      ↓
🗄️ Servidor Web
      ↓
📄 Página Web
```

---

# 🔗 O que é uma URL?

A **URL (Uniform Resource Locator)** é o endereço utilizado para localizar um recurso na Internet.

Exemplo:

```text
https://www.reddit.com
```

A URL permite que o navegador encontre o site ou recurso solicitado.

Podemos pensar na URL como o endereço de uma localização na Internet.

---

# 🧩 Estrutura de um Endereço Web

Um endereço web pode ser dividido em diferentes partes.

Exemplo:

```text
https://www.reddit.com
```

Podemos representar assim:

```text
https://   www.   reddit   .com
   │        │       │       │
Protocolo  Web    Domínio  Extensão
```

## 🔐 HTTPS

O **HTTPS (HyperText Transfer Protocol Secure)** é utilizado para realizar uma comunicação mais segura entre o navegador e o servidor.

```text
💻 Navegador
      │
      │ HTTPS
      ↓
🗄️ Servidor Web
```

---

## 🌐 WWW

O **WWW (World Wide Web)** significa **World Wide Web**.

Tradicionalmente, o `www` era utilizado para indicar um serviço relacionado à Web.

Exemplo:

```text
www.reddit.com
```

Atualmente, muitos sites podem funcionar com ou sem o `www`.

---

## 🏷️ Nome de Domínio

O domínio é o nome utilizado para identificar um site.

Exemplo:

```text
reddit.com
```

O domínio é mais fácil de memorizar do que um endereço IP.

Os nomes de domínio são registrados e administrados dentro de um sistema global de nomes de domínio.

A **ICANN (Internet Corporation for Assigned Names and Numbers)** coordena aspectos importantes relacionados ao sistema global de nomes de domínio.

---

# 🏷️ Extensões de Domínio

As extensões ajudam a identificar a categoria ou finalidade original de um domínio.

Alguns exemplos são:

| Extensão | Uso tradicional |
| -------- | --------------- |
| `.com`   | Comercial       |
| `.net`   | Redes           |
| `.org`   | Organizações    |
| `.edu`   | Educação        |

Exemplo:

```text
reddit.com
      │
      └── .com
```

É importante lembrar que o significado e as regras de uso das extensões podem variar conforme o domínio e o país.

---

# 🌐 Domínios e Endereços IP

Os computadores utilizam endereços IP para se comunicar.

Por exemplo:

```text
🌐 192.168.1.10
```

Entretanto, seria difícil para os usuários memorizar o endereço IP de todos os sites que acessam.

Por isso, utilizamos nomes de domínio:

```text
google.com
reddit.com
youtube.com
```

O **DNS (Domain Name System)** faz a tradução entre nomes de domínio e endereços IP.

---

# 🔎 Como Funciona o DNS?

Quando o usuário digita um endereço no navegador, o processo pode ser representado assim:

```text
💻 Usuário digita:

www.exemplo.com
        ↓
🔎 DNS procura o endereço IP
        ↓
🌐 Endereço IP encontrado
        ↓
🗄️ Navegador se conecta ao servidor
        ↓
📄 Página Web é carregada
```

De forma simplificada:

```text
🌐 Nome de domínio
        ↓
🔎 DNS
        ↓
🌐 Endereço IP
        ↓
🗄️ Servidor Web
        ↓
📄 Página Web
```

O DNS funciona de maneira semelhante a uma agenda telefônica.

Em vez de memorizar um número difícil, o usuário utiliza um nome fácil de lembrar.

---

# 🧪 Exemplo de Acesso a um Site

Imagine que o usuário digite:

```text
https://www.exemplo.com
```

O processo pode ser:

```text
1️⃣ Usuário digita a URL
        ↓
2️⃣ Navegador identifica o domínio
        ↓
3️⃣ DNS procura o endereço IP
        ↓
4️⃣ O navegador encontra o servidor
        ↓
5️⃣ O servidor envia os dados
        ↓
6️⃣ A página Web é exibida
```

---

# ⚠️ Problemas de DNS

Um problema de DNS pode impedir o acesso a um site pelo nome de domínio.

Por exemplo:

```text
🌐 Site pelo endereço IP
        ↓
✅ Funciona

🌐 Site pelo nome de domínio
        ↓
❌ Não funciona
```

Nesse caso, pode existir um problema relacionado à resolução de nomes DNS.

O DNS é fundamental porque permite transformar nomes fáceis de memorizar em endereços IP utilizados pelos computadores.

---

# 🧠 Fluxo Geral do Acesso à Web

```text
💻 Usuário
      ↓
🌐 Navegador
      ↓
🔗 URL
      ↓
🏷️ Nome de domínio
      ↓
🔎 DNS
      ↓
🌐 Endereço IP
      ↓
🗄️ Servidor Web
      ↓
📄 Página Web
```

---

# 💡 Principais Lições

* 🌐 A Web é uma das principais formas de acessar informações na Internet.
* 📄 As páginas web são documentos que podem conter textos, imagens, vídeos e outros conteúdos.
* 📝 O HTML é utilizado para estruturar páginas web.
* 🔗 A URL é o endereço utilizado para localizar um site ou recurso na Internet.
* 🏷️ O domínio fornece um nome fácil de memorizar para um site.
* 🌐 Os computadores utilizam endereços IP para se comunicar.
* 🔎 O DNS traduz nomes de domínio em endereços IP.
* 🗄️ O navegador utiliza o endereço IP para localizar o servidor do site.
* ⚠️ Problemas de DNS podem impedir o acesso a um site pelo nome de domínio.
* 🔐 O HTTPS permite uma comunicação mais segura entre o navegador e o servidor.

---

# 🎯 Resumo Final

Para acessar um site, o usuário normalmente utiliza um navegador e digita uma URL.

A URL contém um nome de domínio, que é mais fácil de memorizar do que um endereço IP.

O DNS realiza a tradução:

```text
🏷️ Nome de domínio
        ↓
🔎 DNS
        ↓
🌐 Endereço IP
        ↓
🗄️ Servidor Web
        ↓
📄 Página Web
```

Dessa forma, o usuário pode acessar sites utilizando nomes simples, enquanto os computadores utilizam endereços IP para localizar e se comunicar com os servidores.

🌐 **A Web permite acessar páginas e serviços.**

🔗 **A URL identifica o recurso.**

🏷️ **O domínio fornece um nome fácil de memorizar.**

🔎 **O DNS traduz o domínio para um endereço IP.**

🌐 **O IP permite a comunicação entre os dispositivos.**
