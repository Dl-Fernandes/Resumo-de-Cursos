# 🌐 Modelo OSI (Open Systems Interconnection)

O **Modelo OSI (Open Systems Interconnection)** é um modelo de referência criado pela **ISO (International Organization for Standardization)** no final da década de 1970 para padronizar a comunicação entre computadores e dispositivos de rede.

Diferentemente do **modelo TCP/IP**, que é utilizado na prática pela Internet, o **Modelo OSI** é uma estrutura **teórica** utilizada para compreender como ocorre a comunicação entre sistemas, desenvolver protocolos e facilitar a identificação e solução de problemas de rede.

O modelo divide a comunicação em **sete camadas**, onde cada uma possui uma função específica e trabalha em conjunto com as demais.

---

# 🎯 Objetivos

Nesta aula aprendemos:

* 🌐 O que é o Modelo OSI;
* 🧩 As sete camadas do modelo;
* 📡 A função de cada camada;
* 📦 Como os dados percorrem a rede;
* 🔍 A importância do Modelo OSI para o estudo e diagnóstico de redes.

---

# 🧱 As 7 Camadas do Modelo OSI

```text
🖥️ 7 - Aplicação
🎨 6 - Apresentação
🤝 5 - Sessão
🚚 4 - Transporte
🌐 3 - Rede
🔗 2 - Enlace de Dados
⚡ 1 - Física
```

Cada camada executa uma função específica durante a comunicação entre dispositivos.

---

# ⚡ Camada 1 - Física

A **Camada Física** é responsável pela transmissão dos bits através do meio físico.

Ela define:

* 🔌 Cabos;
* 📡 Sinais elétricos e ópticos;
* 📶 Ondas de rádio;
* 🔗 Conectores;
* ⚙️ Características físicas da comunicação.

**PDU:** Bits

### Exemplos

* Cabo Ethernet
* Fibra óptica
* Wi-Fi (meio físico)
* Repetidores
* Hubs

---

# 🔗 Camada 2 - Enlace de Dados

A **Camada de Enlace** garante a comunicação entre dispositivos conectados na mesma rede local.

Suas funções incluem:

* 📦 Organização dos dados em quadros (Frames);
* 🔍 Detecção de erros;
* 🔄 Controle de acesso ao meio;
* 🏷️ Utilização dos endereços MAC.

**PDU:** Frames (Quadros)

### Exemplos

* Ethernet
* Wi-Fi (IEEE 802.11)
* Switches
* Bridges

---

# 🌐 Camada 3 - Rede

A **Camada de Rede** permite a comunicação entre diferentes redes.

Ela utiliza endereços IP para determinar o melhor caminho para os dados.

Principais funções:

* 🌍 Roteamento;
* 🌐 Endereçamento lógico;
* 📦 Encaminhamento de pacotes.

**PDU:** Pacotes

### Exemplos

* IPv4
* IPv6
* ICMP
* Roteadores

---

# 🚚 Camada 4 - Transporte

A **Camada de Transporte** garante que os dados sejam entregues corretamente ao destino.

Ela realiza:

* 📦 Segmentação dos dados;
* ✅ Controle de erros;
* 🔄 Controle de fluxo;
* 📬 Comunicação entre aplicações.

**PDU:**

* Segmentos (TCP)
* Datagramas (UDP)

### Exemplos

* TCP
* UDP

---

# 🤝 Camada 5 - Sessão

A **Camada de Sessão** controla a comunicação entre aplicações.

Suas principais funções são:

* 🤝 Estabelecer sessões;
* 🔄 Manter a comunicação;
* ⏹️ Encerrar sessões;
* 📌 Sincronizar transmissões.

**PDU:** Dados

### Exemplos

* NetBIOS
* RPC
* SIP

---

# 🎨 Camada 6 - Apresentação

A **Camada de Apresentação** é responsável por preparar os dados para a aplicação.

Ela realiza:

* 🔐 Criptografia;
* 🔓 Descriptografia;
* 📦 Compressão;
* 📂 Descompressão;
* 🌐 Conversão de formatos.

**PDU:** Dados

### Exemplos

* SSL/TLS
* JPEG
* MPEG
* ASCII

---

# 🖥️ Camada 7 - Aplicação

É a camada mais próxima do usuário.

Ela fornece serviços de rede utilizados pelos aplicativos.

Exemplos de serviços:

* 🌍 Navegação na Web;
* 📧 Correio eletrônico;
* 📂 Transferência de arquivos;
* 🌐 Resolução de nomes.

**PDU:** Dados

### Exemplos

* HTTP / HTTPS
* DNS
* FTP
* SMTP
* SSH

---

# 📦 Encapsulamento dos Dados

Durante a transmissão, cada camada adiciona suas próprias informações aos dados.

```text
🖥️ Aplicação
      ↓
🚚 Transporte
      ↓
🌐 Rede
      ↓
🔗 Enlace
      ↓
⚡ Física
```

No dispositivo de destino ocorre o processo inverso, chamado **desencapsulamento**.

---

# 💡 Principais Lições

* 🌐 O Modelo OSI possui sete camadas.
* ⚡ A Camada Física transmite os bits.
* 🔗 A Camada de Enlace utiliza endereços MAC.
* 🌍 A Camada de Rede utiliza endereços IP.
* 🚚 A Camada de Transporte utiliza TCP e UDP.
* 🤝 A Camada de Sessão controla a comunicação entre aplicações.
* 🎨 A Camada de Apresentação realiza criptografia, compressão e conversão de dados.
* 🖥️ A Camada de Aplicação fornece serviços aos programas utilizados pelos usuários.
* 📦 Os dados passam por todas as camadas durante a comunicação.

---

# 📌 Resumo

O **Modelo OSI** é uma referência utilizada para explicar como ocorre a comunicação entre dispositivos em uma rede.

Ele divide esse processo em **sete camadas**, permitindo compreender as funções de cada etapa da transmissão dos dados.

Embora a Internet utilize principalmente o **modelo TCP/IP**, o **Modelo OSI** continua sendo amplamente utilizado no ensino, na documentação técnica e na solução de problemas de redes, tornando-se um dos conceitos mais importantes para profissionais de Tecnologia da Informação.
