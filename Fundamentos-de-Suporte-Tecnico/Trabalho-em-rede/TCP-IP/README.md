# 🌐 Protocolos de Rede

Os **protocolos de rede** são conjuntos de regras que permitem a comunicação correta entre dispositivos conectados a uma rede.

Eles definem como os dados devem ser:

* 📦 Divididos;
* 📡 Enviados;
* 🧭 Encaminhados;
* 🔄 Recebidos;
* ✅ Verificados.

Sem protocolos, os dispositivos não teriam regras comuns para se comunicar.

---

# 🌐 Protocolo IP

O **IP (Internet Protocol)** é responsável pelo endereçamento e pelo encaminhamento dos pacotes de dados.

Ele utiliza endereços IP para identificar o destino dos dados.

```text
📦 Pacote de dados
      ↓
🌐 Endereço IP de destino
      ↓
📡 Roteadores encaminham o pacote
      ↓
💻 Dispositivo correto
```

O IP permite que os dados sejam encaminhados entre diferentes redes.

---

# 🔄 Protocolo TCP

O **TCP (Transmission Control Protocol)** garante uma transmissão confiável dos dados.

Ele ajuda a garantir que os dados:

* 📦 Sejam entregues;
* 🔢 Cheguem na ordem correta;
* 🔄 Sejam retransmitidos quando necessário;
* ✅ Sejam recebidos corretamente.

Quando uma informação é dividida em vários pacotes, o TCP ajuda a controlar e reorganizar esses dados no destino.

```text
💻 Origem
   ↓
📦 Dados divididos em pacotes
   ↓
🌐 Rede
   ↓
💻 Destino
   ↓
🔄 TCP organiza os dados
```

---

# 🌐 TCP/IP

O **TCP/IP** é a combinação de protocolos utilizada para permitir a comunicação entre computadores e redes.

De forma simplificada:

```text
📦 Dados
   ↓
🔄 TCP
Garante a entrega confiável
   ↓
🌐 IP
Identifica e encaminha o destino
   ↓
💻 Dispositivo de destino
```

* 🔄 **TCP:** garante a confiabilidade da transmissão;
* 🌐 **IP:** identifica o destino e encaminha os pacotes.

A combinação TCP/IP é uma das bases do funcionamento da Internet.

---

# 🛠️ Configuração de uma Rede TCP/IP

Para configurar uma rede TCP/IP, normalmente é necessário definir:

## 🌐 Endereço IP

Identifica o dispositivo dentro da rede.

Exemplo:

```text
💻 Computador → 192.168.1.10
📱 Smartphone  → 192.168.1.11
```

O IP pode ser:

* ⚙️ **Estático:** configurado manualmente;
* 📡 **Dinâmico:** atribuído automaticamente pelo DHCP.

---

## 🧩 Máscara de Sub-rede

A máscara ajuda a identificar qual parte do endereço IP representa a rede e qual parte representa o dispositivo.

Exemplo:

```text
Endereço IP:      192.168.1.10
Máscara de rede:  255.255.255.0
```

---

## 📡 Gateway Padrão

O gateway padrão geralmente é o endereço IP do roteador.

Ele permite que o dispositivo se comunique com outras redes e com a Internet.

```text
💻 Computador
      ↓
📡 Gateway
      ↓
📡 Roteador
      ↓
🌐 Internet
```

Exemplo:

```text
192.168.1.1
```

---

## 🔎 DNS

O **DNS (Domain Name System)** traduz nomes de domínio em endereços IP.

```text
google.com
     ↓
🔎 DNS
     ↓
🌐 Endereço IP
     ↓
🗄️ Servidor
```

Isso permite acessar sites utilizando nomes fáceis de memorizar.

---

# 🧪 Testando a Conectividade

O comando `ping` pode ser utilizado para verificar se existe comunicação entre dispositivos.

Exemplo:

```bash
ping 192.168.1.1
```

Também é possível testar um domínio:

```bash
ping google.com
```

O `ping` pode ajudar a verificar:

* 📡 Se existe comunicação;
* 📦 Se os pacotes estão chegando;
* ⏱️ O tempo de resposta;
* ❌ Se existe perda de pacotes.

---

# 🧩 Exemplo de Configuração TCP/IP

Uma configuração de rede pode ser:

```text
💻 Computador

🌐 Endereço IP:
192.168.1.10

🧩 Máscara de sub-rede:
255.255.255.0

📡 Gateway padrão:
192.168.1.1

🔎 DNS:
Servidor DNS configurado
```

O fluxo da comunicação pode ser representado assim:

```text
💻 Dispositivo
      ↓
🌐 Endereço IP
      ↓
🧩 Máscara de sub-rede
      ↓
📡 Gateway
      ↓
🔎 DNS
      ↓
🌐 Internet
```

---

# 🧠 Fluxo Geral da Comunicação TCP/IP

```text
💻 Dispositivo de origem
        ↓
📦 Dados são divididos em pacotes
        ↓
🌐 IP identifica o destino
        ↓
📡 Roteadores encaminham os pacotes
        ↓
🔎 DNS traduz nomes de domínio
        ↓
🔄 TCP garante a entrega confiável
        ↓
💻 Dispositivo de destino
```

---

# 💡 Principais Lições

* 🌐 Protocolos de rede definem regras para a comunicação entre dispositivos.
* 🌐 O IP identifica os destinos e encaminha os pacotes.
* 🔄 O TCP garante uma transmissão confiável.
* 📦 Os dados podem ser divididos em vários pacotes.
* 🧩 A máscara de sub-rede ajuda a identificar a rede.
* 📡 O gateway permite a comunicação com outras redes.
* 🔎 O DNS traduz nomes de domínio em endereços IP.
* 🧪 O comando `ping` ajuda a testar a conectividade.
* 🌐 TCP/IP é fundamental para o funcionamento da Internet.

---

# 🎯 Resumo Final

A comunicação em rede depende de protocolos que definem como os dispositivos devem trocar informações.

O **IP** é responsável pelo endereçamento e encaminhamento dos pacotes.

O **TCP** garante que os dados sejam entregues de forma confiável e na ordem correta.

Para configurar uma rede TCP/IP, normalmente são necessários:

```text
🌐 Endereço IP
        ↓
🧩 Máscara de sub-rede
        ↓
📡 Gateway padrão
        ↓
🔎 Servidor DNS
        ↓
🔄 TCP/IP
        ↓
📦 Comunicação entre dispositivos
```

Compreender esses conceitos é fundamental para quem deseja trabalhar com:

* 🛠️ Suporte técnico;
* 🌐 Redes de computadores;
* 🖥️ Administração de sistemas;
* ☁️ Computação em nuvem;
* 🔐 Segurança da informação.
