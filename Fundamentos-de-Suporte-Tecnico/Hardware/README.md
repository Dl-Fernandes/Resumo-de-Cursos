# 🖥️ Hardware

Guia de estudos e documentação técnica com os principais conceitos apresentados no módulo **Hardware**, do curso **Fundamentos do Suporte Técnico**, oferecido pelo **Google** na plataforma **Coursera**.

Neste módulo foram abordados os principais componentes físicos do computador, suas funções, formas de comunicação e critérios de compatibilidade entre hardware.

---

## 🎯 Objetivos

Ao final deste módulo é possível compreender:

- Como a CPU processa instruções.
- Como ocorre a comunicação entre a CPU e a memória RAM.
- A função do Controlador de Memória (MCC).
- Os diferentes tipos de memória RAM.
- A importância da compatibilidade entre CPU, memória e placa-mãe.
- A função do chipset e da placa-mãe.
- Os principais padrões de expansão utilizados atualmente.

---

# 🧠 Controlador de Memória (Memory Controller Chip - MCC)

O **Controlador de Memória (MCC)** atua como uma ponte entre a **CPU** e a **memória RAM**.

Sua principal função é localizar os dados solicitados pelo processador e entregá-los de forma rápida e organizada.

### Funcionamento

1. A CPU envia o endereço da informação através do **Barramento de Endereço (Address Bus)**.
2. O MCC localiza essa informação na memória RAM.
3. Os dados são enviados para a CPU através do **Barramento Externo de Dados (External Data Bus - EDB)**.

Sem o controlador de memória, a CPU teria dificuldade em localizar informações específicas dentro da RAM, que pode armazenar milhões de posições de memória.

---

# 🖥️ CPU (Central Processing Unit)

A **CPU** é considerada o cérebro do computador.

Sua função é interpretar e executar instruções enviadas pelos programas.

Todo software é dividido em pequenas instruções que a CPU executa continuamente.

Entre essas operações estão:

- Soma
- Subtração
- Comparação
- Cópia de dados
- Operações lógicas

Essas instruções são conhecidas como **Instruction Set (Conjunto de Instruções)**.

---

## 🏭 Fabricantes

Os principais fabricantes de processadores são:

- Intel
- AMD
- Qualcomm

Cada fabricante possui arquiteturas e soquetes próprios.

---

## 🔌 Compatibilidade entre CPU e Placa-mãe

Antes de instalar um processador é necessário verificar a compatibilidade do soquete.

### LGA (Land Grid Array)

- Os pinos ficam na placa-mãe.
- A CPU possui apenas contatos metálicos.
- Muito utilizado pela Intel.

### PGA (Pin Grid Array)

- Os pinos ficam no processador.
- O socket da placa-mãe possui apenas os contatos.
- Muito utilizado pela AMD em diversas gerações.

> CPU e placa-mãe precisam possuir o mesmo tipo de socket para funcionarem corretamente.

---

## ⚙️ Arquitetura 32 bits e 64 bits

A arquitetura define a quantidade de dados que a CPU consegue processar simultaneamente.

### 32 bits

- Processa blocos de 32 bits.
- Geralmente suporta até 4 GB de memória RAM.
- Encontrada em computadores mais antigos.

### 64 bits

- Processa blocos de 64 bits.
- Suporta grandes quantidades de memória RAM.
- Possui maior desempenho em aplicações modernas.

---

## ❄️ Sistema de Resfriamento

Durante seu funcionamento a CPU produz calor.

Para evitar superaquecimento são utilizados:

- Dissipador de calor
- Cooler (ventilador)
- Pasta térmica

Sem refrigeração adequada o desempenho pode diminuir e ocorrer danos ao hardware.

---

# 💾 Memória RAM

A **RAM (Random Access Memory)** é a memória de curto prazo do computador.

Ela armazena temporariamente os programas e dados utilizados pelo processador.

Por ser uma memória **volátil**, todas as informações são perdidas quando o computador é desligado.

---

## 📌 Funções da RAM

- Armazenar programas em execução.
- Fornecer acesso rápido às informações utilizadas pela CPU.
- Permitir a execução simultânea de vários programas.

Quanto maior a quantidade de memória RAM, maior tende a ser a capacidade de multitarefa do computador.

---

## 📚 Evolução da Memória RAM

As principais gerações são:

- DRAM (Dynamic RAM)
- SDRAM (Synchronous DRAM)
- DDR SDRAM
- DDR2
- DDR3
- DDR4
- DDR5

Cada nova geração oferece:

- Maior velocidade.
- Menor consumo de energia.
- Maior capacidade de armazenamento.

---

## 🔗 Compatibilidade da RAM

Ao instalar memória RAM é necessário verificar:

- Tipo da memória (DDR3, DDR4, DDR5...)
- Frequência suportada.
- Quantidade máxima suportada.
- Número de pinos.
- Compatibilidade com a placa-mãe.

---

# 🖥️ Placa-mãe (Motherboard)

A placa-mãe é responsável por conectar todos os componentes do computador.

Ela permite que CPU, memória, armazenamento e periféricos se comuniquem corretamente.

---

## ⚙️ Chipset

O chipset controla a comunicação entre os componentes do computador.

Historicamente ele era dividido em duas partes.

### Northbridge

Responsável pela comunicação com dispositivos de alta velocidade.

Exemplos:

- CPU
- Memória RAM
- Placa de vídeo

Atualmente essa função normalmente está integrada ao próprio processador.

### Southbridge

Gerencia dispositivos de entrada e saída.

Exemplos:

- HD
- SSD
- USB
- Áudio
- Rede
- BIOS

---

# 🔌 Slots de Expansão

A placa-mãe permite adicionar novos dispositivos através dos slots de expansão.

O padrão mais utilizado atualmente é o **PCI Express (PCIe)**.

Ele é utilizado para instalar:

- Placas de vídeo.
- Placas de rede.
- Placas de captura.
- SSDs NVMe (em alguns formatos).

Quanto maior o número de pistas (*lanes*), maior será a velocidade de comunicação.

---

# 📐 Form Factor (Fator de Forma)

O **Form Factor** determina o tamanho físico da placa-mãe.

Os formatos mais comuns são:

| Formato | Características |
|----------|-----------------|
| ATX | Mais expansível e utilizado em desktops. |
| Micro-ATX | Menor que o ATX, mantendo boa capacidade de expansão. |
| Mini-ITX | Compacto e utilizado em computadores pequenos. |
| Nano-ITX | Muito compacto. |
| Pico-ITX | Utilizado em sistemas embarcados e aplicações específicas. |

O tamanho influencia:

- Quantidade de slots PCIe.
- Quantidade de módulos de memória RAM.
- Espaço disponível no gabinete.
- Possibilidades de expansão.

---

# 📖 Resumo

Neste módulo foram estudados os principais componentes de hardware responsáveis pelo funcionamento do computador.

Foram apresentados o funcionamento da CPU, do Controlador de Memória (MCC), da memória RAM e da placa-mãe, além dos conceitos de compatibilidade entre hardware, arquitetura de 32 e 64 bits, chipset, PCI Express e fatores de forma das placas-mãe.

Esses conhecimentos são fundamentais para compreender como os componentes físicos de um computador trabalham em conjunto para executar programas e processar informações.

---

---

# 💽 Armazenamento de Dados

Os dispositivos de armazenamento são responsáveis por guardar permanentemente os dados do computador, como sistema operacional, programas, documentos, fotos e vídeos.

Ao contrário da memória RAM, o armazenamento é **não volátil**, ou seja, os dados permanecem gravados mesmo após o desligamento do computador.

---

## 📏 Unidades de Medida de Dados

As informações armazenadas em um computador são medidas utilizando unidades padronizadas.

| Unidade | Equivalência |
|----------|--------------|
| Bit (b) | Menor unidade de informação (0 ou 1). |
| Byte (B) | 8 bits. |
| Kilobyte (KB) | 1.024 bytes. |
| Megabyte (MB) | 1.024 KB. |
| Gigabyte (GB) | 1.024 MB. |
| Terabyte (TB) | 1.024 GB. |
| Petabyte (PB) | 1.024 TB. |
| Exabyte (EB) | 1.024 PB. |
| Zettabyte (ZB) | 1.024 EB. |
| Yottabyte (YB) | 1.024 ZB. |

---

## 📚 Sistema Decimal × Sistema Binário

Existem duas formas de representar capacidades de armazenamento.

### Sistema Decimal

Utilizado principalmente pelos fabricantes de discos.

| Prefixo | Valor |
|----------|-------|
| KB | 1.000 bytes |
| MB | 1.000² bytes |
| GB | 1.000³ bytes |
| TB | 1.000⁴ bytes |

---

### Sistema Binário

Utilizado pelos sistemas operacionais e engenharia da computação.

| Prefixo | Valor |
|----------|-------|
| KiB | 1.024 bytes |
| MiB | 1.024² bytes |
| GiB | 1.024³ bytes |
| TiB | 1.024⁴ bytes |

> O sistema binário oferece maior precisão na representação das capacidades de armazenamento.

---

# 💿 Dispositivos de Armazenamento

Os principais dispositivos utilizados atualmente são os HDDs e SSDs.

---

## HDD (Hard Disk Drive)

O HDD utiliza discos magnéticos que giram em alta velocidade.

Os dados são lidos e gravados por um braço mecânico.

### Características

- Maior capacidade por menor custo.
- Possui partes móveis.
- Velocidade medida em RPM (Rotações por Minuto).
- Mais sensível a impactos físicos.

---

## SSD (Solid State Drive)

O SSD utiliza memória flash para armazenar dados.

Como não possui partes móveis, oferece desempenho muito superior ao HDD.

### Características

- Muito mais rápido.
- Menor consumo de energia.
- Mais resistente a impactos.
- Funcionamento silencioso.
- Custo por gigabyte mais elevado.

---

# 🔌 Interfaces de Conexão

A interface determina como o dispositivo de armazenamento se comunica com o computador.

---

## SATA (Serial ATA)

A interface SATA é a mais utilizada em HDDs e SSDs tradicionais.

Características:

- Boa compatibilidade.
- Permite Hot Swap (troca com o equipamento ligado, quando suportado).
- Velocidade inferior ao NVMe.

---

## NVMe (Non-Volatile Memory Express)

O NVMe foi desenvolvido especificamente para SSDs.

Ele utiliza as pistas PCI Express (PCIe), oferecendo velocidades muito superiores ao SATA.

### Vantagens

- Maior velocidade de leitura.
- Maior velocidade de gravação.
- Menor latência.
- Melhor desempenho geral.

---

# 🔋 Fonte de Alimentação (Power Supply Unit - PSU)

A fonte de alimentação converte a corrente alternada (CA) da rede elétrica em corrente contínua (CC), utilizada pelos componentes internos do computador.

Além disso, fornece diferentes níveis de tensão para cada componente.

---

## Funções da Fonte

- Converter corrente alternada em corrente contínua.
- Distribuir energia para os componentes internos.
- Proteger o computador contra variações elétricas.

---

## Tensões Utilizadas

| Tensão | Componentes |
|---------|-------------|
| 3,3 V | Chipsets e módulos de memória. |
| 5 V | Dispositivos lógicos e alguns controladores. |
| 12 V | CPU, placas de vídeo, discos e coolers. |

---

## Compatibilidade da Fonte

Ao escolher uma fonte de alimentação é necessário considerar:

- Potência necessária.
- Formato da placa-mãe (ATX, Micro-ATX, Mini-ITX).
- Quantidade de dispositivos instalados.
- Consumo da CPU.
- Consumo da GPU.

---

## Conector Principal ATX

O padrão atual utiliza um conector principal de:

- 24 pinos

Modelos antigos utilizavam:

- 20 pinos

---

# 🌎 Tensão Elétrica

A tensão elétrica varia conforme o país.

Os padrões mais comuns são:

- 110–127 V
- 220–240 V

Utilizar uma tensão incompatível pode impedir o funcionamento do computador ou causar danos aos componentes.

---

# 🖱️ Periféricos

Periféricos são dispositivos externos conectados ao computador para adicionar funcionalidades.

Exemplos:

- Mouse
- Teclado
- Monitor
- Impressora
- Webcam
- Scanner

---

# 🔌 Conectores USB

O USB (Universal Serial Bus) é o padrão mais utilizado para conectar periféricos.

| Padrão | Cor (geralmente) | Velocidade |
|---------|------------------|------------|
| USB 2.0 | Preto | 480 Mbps |
| USB 3.0 | Azul | 5 Gbps |
| USB 3.1 | Azul-petróleo | 10 Gbps |

As portas USB são retrocompatíveis.

---

## USB Tipo C

O USB-C tornou-se o padrão mais moderno.

Pode transmitir:

- Dados
- Vídeo
- Áudio
- Energia

Também é utilizado pelo padrão USB4/Thunderbolt.

---

# 🖥️ Conectores de Vídeo

Os principais conectores para monitores são:

### DVI

- Transmite apenas vídeo.

### HDMI

- Transmite áudio e vídeo.

### DisplayPort

- Transmite áudio e vídeo.
- Muito utilizado em monitores de alto desempenho.

---

# 🌐 Conectores de Rede

Os principais conectores utilizados em redes são:

| Conector | Utilização |
|-----------|------------|
| RJ-11 | Telefonia (POTS/DSL). |
| RJ-45 | Redes Ethernet. |
| Fibra Óptica | Internet de alta velocidade. |

---

# 🔧 Outros Conectores

### Molex

Utilizado para alimentação de dispositivos internos, principalmente em equipamentos mais antigos.

### DB9

Conector serial encontrado em equipamentos legados.

### Lightning

Conector proprietário utilizado pela Apple.

---

# 📖 Resumo

Neste módulo foram estudados os principais componentes físicos responsáveis pelo funcionamento do computador.

Também foram abordados os dispositivos de armazenamento (HDD e SSD), unidades de medida de dados, fontes de alimentação, periféricos, interfaces de conexão, portas USB, conectores de vídeo e comunicação, além das diferenças entre os principais padrões utilizados atualmente.

Esses conhecimentos fornecem uma base sólida para compreender a montagem, manutenção e compatibilidade de computadores modernos.

---

## 🔗 Atalho de Navegação

⬅️ [Voltar para Fundamentos do Suporte Técnico](../README.md)
