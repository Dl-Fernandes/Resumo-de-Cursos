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

## 🔗 Atalho de Navegação

⬅️ [Voltar para Fundamentos do Suporte Técnico](../README.md)
