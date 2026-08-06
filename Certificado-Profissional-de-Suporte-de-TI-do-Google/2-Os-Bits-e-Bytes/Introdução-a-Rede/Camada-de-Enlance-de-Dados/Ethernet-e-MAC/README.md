# 🌐 Ethernet e Endereçamento MAC

## 🎯 Objetivos

Nesta aula, aprendemos os fundamentos da tecnologia **Ethernet**, o funcionamento da **Camada de Enlace de Dados (Camada 2 do Modelo OSI)** e a importância do **endereço MAC** para a comunicação em redes locais.

Também vimos:

- O que é Ethernet;
- A evolução das redes Ethernet;
- O conceito de domínio de colisão;
- Como funciona o protocolo CSMA/CD;
- O que é um endereço MAC;
- Como é formada a estrutura de um endereço MAC;
- O significado do OUI;
- Como o endereço MAC identifica dispositivos;
- Como o CRC verifica a integridade dos dados;
- A importância da Camada de Enlace para a comunicação em redes locais.

---

# 🌐 O que é Ethernet?

O **Ethernet** é a tecnologia de rede local (LAN) mais utilizada no mundo.

Padronizado em **1983**, ele continua sendo amplamente utilizado em:

- 🏢 Empresas;
- 🖥️ Escritórios;
- 🏠 Redes domésticas;
- ☁️ Data Centers;
- 🌐 Infraestruturas corporativas.

Sua principal função é permitir que dispositivos conectados à mesma rede local possam trocar informações de maneira rápida, eficiente e confiável.

---

# 🏛️ História do Ethernet

As primeiras redes Ethernet utilizavam um único cabo compartilhado entre todos os computadores.

Nesse modelo:

- Todos os computadores compartilhavam o mesmo meio físico;
- Apenas um dispositivo podia transmitir por vez;
- Caso dois computadores transmitissem simultaneamente, ocorria uma colisão.

Esse ambiente era conhecido como **Domínio de Colisão**.

---

# 💥 Domínio de Colisão

Um **Domínio de Colisão** é uma área da rede onde apenas um dispositivo pode transmitir dados por vez.

Se dois dispositivos transmitirem ao mesmo tempo:

- ocorre uma colisão;
- os dados precisam ser retransmitidos;
- a rede fica mais lenta.

Representação:

```text
Computador A
        │
Computador B
        │
Computador C
        │
Computador D

Todos compartilham o mesmo meio físico
```

Nas redes modernas, os **switches** praticamente eliminaram esse problema.

Cada porta do switch representa um domínio de colisão independente.

---

# 📡 CSMA/CD

Para evitar colisões nas primeiras redes Ethernet foi criado o protocolo:

**CSMA/CD**

(Carrier Sense Multiple Access with Collision Detection)

Ele funciona da seguinte forma:

1. O dispositivo verifica se o meio está livre.
2. Se estiver livre, transmite os dados.
3. Caso detecte uma colisão, interrompe a transmissão.
4. Aguarda um tempo aleatório.
5. Tenta transmitir novamente.

Esse mecanismo permitia que vários dispositivos compartilhassem o mesmo cabo de forma organizada.

---

# 🔗 Camada de Enlace de Dados

A Camada de Enlace é responsável por realizar a comunicação entre dispositivos que estão na mesma rede local.

Suas principais funções são:

- Encapsular os dados em quadros (frames);
- Identificar o dispositivo de origem;
- Identificar o dispositivo de destino;
- Detectar erros de transmissão;
- Controlar o acesso ao meio físico.

Ela atua diretamente sobre a Camada Física.

---

# 📦 Quadros (Frames)

Na Camada de Enlace, os dados são organizados em estruturas chamadas **Frames (Quadros)**.

Um quadro Ethernet normalmente contém:

- Endereço MAC de origem;
- Endereço MAC de destino;
- Dados transmitidos;
- Informações de controle;
- CRC (verificação de erros).

Representação simplificada:

```text
+---------------------------------------------+
| MAC Destino | MAC Origem | Dados | CRC |
+---------------------------------------------+
```

---

# 🆔 O que é um Endereço MAC?

Todo dispositivo conectado a uma rede possui um **Endereço MAC (Media Access Control Address)**.

O endereço MAC identifica **fisicamente** uma interface de rede.

Ele é gravado pelo fabricante da placa de rede e, normalmente, não muda.

Cada placa de rede possui um endereço único no mundo.

---

# 🧱 Estrutura do Endereço MAC

Um endereço MAC possui:

- 48 bits;
- 6 grupos de 2 caracteres hexadecimais.

Exemplo:

```text
00:1A:2B:3C:4D:5E
```

ou

```text
00-1A-2B-3C-4D-5E
```

Cada grupo representa parte do identificador único do dispositivo.

---

# 🏭 OUI (Organizationally Unique Identifier)

Os três primeiros grupos do endereço MAC correspondem ao:

**OUI (Organizationally Unique Identifier)**

Eles identificam o fabricante da placa de rede.

Exemplo:

```text
00:1A:2B
```

Pode identificar fabricantes como:

- Intel;
- Dell;
- HP;
- Cisco;
- TP-Link;
- Realtek;
- Broadcom.

Os três últimos grupos são exclusivos para cada dispositivo produzido pelo fabricante.

Assim, dois equipamentos nunca possuem o mesmo endereço MAC.

---

# 📨 Como o Endereço MAC Funciona?

Quando um computador envia um quadro Ethernet:

Ele inclui:

- MAC de origem;
- MAC de destino.

Todos os dispositivos da rede recebem esse quadro.

Entretanto, apenas o dispositivo cujo MAC corresponde ao endereço de destino aceita os dados.

Os demais simplesmente ignoram o quadro.

Representação:

```text
Switch
   │
 ├── PC A
 ├── PC B
 ├── PC C
 └── PC D

Quadro destinado ao PC C

Somente o PC C processa os dados.
```

---

# 🛡️ Integridade dos Dados (CRC)

Durante a transmissão podem ocorrer erros devido a:

- interferências;
- ruídos elétricos;
- problemas físicos no cabo.

Para detectar esses erros, o Ethernet utiliza o:

**CRC (Cyclic Redundancy Check)**

ou

**Verificação por Redundância Cíclica**.

O CRC calcula um valor matemático baseado nos dados transmitidos.

Quando o quadro chega ao destino:

- Um novo cálculo é realizado.
- O resultado é comparado com o valor enviado.

Se os valores forem diferentes:

- significa que houve erro na transmissão;
- o quadro é descartado.

---

# 🔄 Fluxo Simplificado da Comunicação Ethernet

```text
Aplicação
      ↓
Camada de Rede
      ↓
Camada de Enlace
      ↓
Frame Ethernet
      ↓
Camada Física
      ↓
Cabo de Rede
      ↓
Switch
      ↓
Dispositivo Destino
```

---

# 🏢 Ethernet nas Redes Modernas

Hoje as redes Ethernet utilizam switches.

Isso trouxe diversas vantagens:

- ✅ Eliminação das colisões;
- ⚡ Maior velocidade;
- 📈 Melhor desempenho;
- 🔒 Comunicação mais eficiente;
- 📡 Links dedicados para cada dispositivo.

Mesmo assim, os conceitos de domínio de colisão e CSMA/CD continuam importantes para compreender a evolução das redes.

---

# 💡 Exemplo Prático

Imagine uma empresa com quatro computadores conectados a um switch.

Quando o Computador A deseja enviar um arquivo ao Computador C:

1. O computador cria um quadro Ethernet.
2. Adiciona o MAC de origem e o MAC de destino.
3. O switch identifica em qual porta está o Computador C.
4. O quadro é enviado apenas para essa porta.
5. O Computador C recebe e verifica o CRC.
6. Se os dados estiverem íntegros, o arquivo é processado.

Todo esse processo acontece em poucos milissegundos.

---

# 📌 Principais Conceitos

| Conceito | Descrição |
|----------|-----------|
| 🌐 Ethernet | Tecnologia mais utilizada em redes locais (LAN). |
| 💥 Domínio de Colisão | Área onde apenas um dispositivo pode transmitir por vez. |
| 📡 CSMA/CD | Protocolo que detecta e controla colisões em redes Ethernet antigas. |
| 🆔 Endereço MAC | Identificador físico único da interface de rede. |
| 🏭 OUI | Parte do endereço MAC que identifica o fabricante. |
| 📦 Frame | Estrutura utilizada para transportar dados na Camada de Enlace. |
| 🛡️ CRC | Método para detectar erros durante a transmissão de dados. |
| 🔗 Camada de Enlace | Responsável pela comunicação entre dispositivos na mesma rede local. |

---

# 📝 Resumo

O **Ethernet** é a principal tecnologia utilizada em redes locais e atua na **Camada de Enlace de Dados**, permitindo a comunicação entre dispositivos conectados à mesma rede.

Nas primeiras implementações, todos os computadores compartilhavam o mesmo meio físico, tornando necessário o uso do **CSMA/CD** para detectar e controlar colisões.

Cada interface de rede possui um **endereço MAC**, um identificador físico único de 48 bits que permite que os dispositivos reconheçam corretamente o destinatário dos quadros Ethernet.

Os **frames Ethernet** incluem os endereços MAC de origem e destino, além do **CRC**, que garante a integridade dos dados transmitidos.

Atualmente, os **switches** praticamente eliminaram os domínios de colisão, tornando as redes Ethernet muito mais rápidas, estáveis e eficientes.

---

# 🎯 Conclusão

A tecnologia **Ethernet** é a base da maioria das redes locais modernas.

Compreender conceitos como **Camada de Enlace**, **endereços MAC**, **frames Ethernet**, **CSMA/CD**, **CRC** e **domínio de colisão** é fundamental para qualquer profissional que deseja atuar com redes de computadores ou suporte técnico.

Esses conceitos servem de base para o entendimento de protocolos mais avançados e para o funcionamento das redes utilizadas atualmente em empresas, residências e data centers.
