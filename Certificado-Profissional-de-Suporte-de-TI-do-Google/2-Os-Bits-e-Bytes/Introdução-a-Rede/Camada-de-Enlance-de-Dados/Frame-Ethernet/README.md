# 🖼️ Frame Ethernet

## 📖 Apresentação

O **Frame Ethernet (Quadro Ethernet)** é a estrutura utilizada pelo padrão Ethernet para transportar dados entre dispositivos em uma rede local (LAN).

Sempre que um computador envia informações pela rede utilizando Ethernet, os dados são organizados em um quadro contendo informações necessárias para que o destinatário receba os dados corretamente e para que a integridade da transmissão possa ser verificada.

Compreender a estrutura de um quadro Ethernet é fundamental para entender como ocorre a comunicação na **Camada de Enlace de Dados** do modelo TCP/IP e do modelo OSI.

---

# 🎯 Objetivos

Ao concluir esta aula, você será capaz de:

- 📦 Entender o que é um Frame Ethernet;
- 🏷️ Identificar os principais campos de um quadro Ethernet;
- 🔌 Compreender a função dos endereços MAC;
- 📡 Entender como o protocolo Ethernet identifica o tipo de informação transportada;
- 🛡️ Compreender como o CRC ajuda a detectar erros durante a transmissão.

---

# 🌐 O que é um Frame Ethernet?

Um **Frame Ethernet** é uma estrutura organizada de informações utilizada para transportar dados entre dispositivos conectados a uma rede Ethernet.

Além dos dados da aplicação, o quadro contém informações importantes, como:

- 📍 Endereço MAC de origem;
- 📍 Endereço MAC de destino;
- 📦 Tipo dos dados transportados;
- 🛡️ Informações para verificar a integridade da transmissão.

Essas informações permitem que os dispositivos da rede saibam para onde enviar os dados e verifiquem se eles chegaram corretamente.

---

# 🧩 Estrutura do Frame Ethernet

Um quadro Ethernet é composto pelos seguintes campos:

```text
┌──────────┬──────────┬──────────┬──────────┬──────────────┬────────────┐
│Preâmbulo │ MAC Dest │ MAC Orig │ EtherType│   Payload    │    FCS     │
└──────────┴──────────┴──────────┴──────────┴──────────────┴────────────┘
```

Cada campo possui uma função específica durante a transmissão.

---

# 🔹 Principais Componentes

## 📡 Preâmbulo

O **Preâmbulo** possui **8 bytes**.

Sua função é sincronizar o dispositivo que receberá o quadro.

O último byte recebe o nome de **SFD (Start Frame Delimiter)**, indicando o início do quadro Ethernet.

---

## 🎯 Endereço MAC de Destino

Este campo contém o endereço MAC do dispositivo que deverá receber os dados.

Cada endereço MAC possui **48 bits (6 bytes)**.

Exemplo:

```text
00:1A:2B:3C:4D:5E
```

---

## 💻 Endereço MAC de Origem

Identifica o dispositivo que enviou o quadro.

Também possui **48 bits (6 bytes)**.

---

## 📦 EtherType

O campo **EtherType** informa qual protocolo está sendo transportado dentro do quadro Ethernet.

Alguns exemplos são:

- 🌐 IPv4
- 🌍 IPv6
- 📡 ARP

Em algumas redes esse campo pode ser substituído por um cabeçalho **VLAN**, utilizado para segmentação lógica da rede.

---

## 📄 Payload

O **Payload** contém os dados reais transmitidos.

Seu tamanho normalmente varia entre:

- Mínimo: **46 bytes**
- Máximo: **1500 bytes**

É nessa área que são transportadas as informações da camada superior.

---

## 🛡️ FCS (Frame Check Sequence)

O **FCS** é o último campo do quadro Ethernet.

Ele possui **4 bytes** e contém um valor calculado utilizando o algoritmo **CRC (Cyclic Redundancy Check)**.

Sua função é verificar se os dados chegaram sem erros durante a transmissão.

---

# 🔄 Como Funciona o CRC?

O **CRC (Cyclic Redundancy Check)** é um mecanismo de detecção de erros.

Seu funcionamento pode ser resumido da seguinte forma:

1. 💻 O dispositivo emissor calcula um valor CRC.
2. 📦 Esse valor é enviado junto com o quadro.
3. 💻 O dispositivo receptor calcula novamente o CRC.
4. 🔍 Os dois valores são comparados.
5. ✅ Se forem iguais, o quadro é aceito.
6. ❌ Se forem diferentes, o quadro é descartado.

```text
💻 Emissor
      │
Calcula CRC
      │
      ▼
📦 Frame Ethernet
      │
      ▼
💻 Receptor
      │
Recalcula CRC
      │
      ▼
Valores iguais?
   │        │
  Sim      Não
   │        │
Aceita   Descarta
```

---

# ⚠️ O Ethernet Corrige Erros?

Não.

O protocolo Ethernet **apenas detecta erros**, utilizando o CRC.

Caso um erro seja encontrado:

- ❌ O quadro é descartado;
- 🔄 A retransmissão será realizada por protocolos de camadas superiores, como o **TCP**, quando necessário.

---

# 💡 Principais Lições

- 📦 O Frame Ethernet é a estrutura utilizada para transportar dados em redes Ethernet.
- 📡 O Preâmbulo sincroniza os dispositivos antes da transmissão.
- 🎯 O endereço MAC de destino identifica quem receberá o quadro.
- 💻 O endereço MAC de origem identifica quem enviou os dados.
- 🌐 O campo EtherType informa qual protocolo está sendo transportado.
- 📄 O Payload contém os dados da comunicação.
- 🛡️ O FCS utiliza CRC para detectar erros de transmissão.
- 🔄 O Ethernet detecta erros, mas não realiza sua correção.

---

# 🎯 Resumo

O **Frame Ethernet** é a unidade de comunicação da tecnologia Ethernet.

Ele organiza todas as informações necessárias para que um dispositivo envie dados a outro dentro de uma rede local.

Além dos dados transmitidos, o quadro contém informações de identificação, sincronização e verificação de integridade.

O uso do **CRC** torna a comunicação mais confiável ao detectar erros durante a transmissão, garantindo que dados corrompidos não sejam processados pelos dispositivos da rede.

Compreender o funcionamento do Frame Ethernet é um dos primeiros passos para entender como ocorre a comunicação na **Camada de Enlace de Dados**, sendo um conhecimento essencial para profissionais de Redes e Infraestrutura de TI.
