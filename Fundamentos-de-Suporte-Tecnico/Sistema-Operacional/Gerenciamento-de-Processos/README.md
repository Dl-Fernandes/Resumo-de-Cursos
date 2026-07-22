
# ⚙️ Gerenciamento de Processos

O gerenciamento de processos é uma das principais funções do kernel e é fundamental para o funcionamento eficiente do sistema operacional.

O kernel controla a criação, execução, organização e encerramento dos processos, distribuindo os recursos disponíveis do computador entre eles.

---

## 📄 Programas e Processos

Um **programa** é um conjunto de instruções armazenado no computador.

Um **processo** é um programa em execução.

Por exemplo, o navegador Google Chrome é um programa. Quando ele é aberto, o sistema operacional cria um ou mais processos para executar suas funções.

É possível ter vários processos relacionados ao mesmo programa funcionando simultaneamente, como:

- 🌐 Várias janelas do navegador;
- 📑 Diferentes abas;
- 🧩 Extensões;
- 🔄 Processos executados em segundo plano.

Para executar um processo, o kernel precisa alocar recursos limitados do computador, como:

- 🧠 Memória RAM;
- ⚙️ CPU;
- 💽 Armazenamento;
- 🔌 Dispositivos de entrada e saída.

---

# 🧠 Gerenciamento de Recursos

O computador possui uma quantidade limitada de recursos.

Por isso, o kernel precisa gerenciar esses recursos para que vários processos possam ser executados sem que um único processo utilize toda a capacidade disponível.

O kernel é responsável por:

- ➕ Criar processos;
- 📅 Agendar processos;
- ▶️ Executar processos;
- ⏸️ Suspender processos;
- 🛑 Encerrar processos;
- ♻️ Liberar os recursos utilizados pelos processos.

Quando um processo é encerrado, os recursos utilizados por ele podem ser liberados e reutilizados por outros processos.

---

# ⏱️ Time Slice (Fatia de Tempo)

A CPU executa as instruções de um processo por um intervalo muito curto de tempo chamado **time slice**.

Depois desse intervalo, o kernel pode interromper temporariamente o processo e permitir que outro processo utilize a CPU.

Esse processo ocorre rapidamente e de forma contínua.

Embora a CPU execute os processos individualmente, a velocidade das trocas cria a impressão de que vários processos estão sendo executados simultaneamente.

---

# 📅 Escalonamento de Processos

O **escalonamento de processos** é o mecanismo utilizado pelo kernel para decidir qual processo receberá acesso à CPU e por quanto tempo.

Para tomar essa decisão, os algoritmos de escalonamento podem considerar:

- ⭐ Prioridade do processo;
- ⏱️ Tempo que o processo já utilizou a CPU;
- ⏳ Tempo de espera;
- ▶️ Estado do processo;
- ⚙️ Políticas específicas do sistema operacional.

O objetivo é distribuir o tempo de processamento de maneira eficiente e justa, mantendo o sistema responsivo.

---

# 🧮 Algoritmos de Escalonamento

Um algoritmo de escalonamento é um conjunto de regras utilizado pelo kernel para determinar:

- ▶️ Qual processo será executado em seguida;
- ⏱️ Por quanto tempo ele utilizará a CPU;
- 🔄 Quando ocorrerá a troca para outro processo.

---

## 📥 FIFO (First In, First Out)

Executa os processos na ordem em que chegaram.

O primeiro processo a entrar na fila é o primeiro a ser executado.

---

## 🔄 Round Robin

Cada processo recebe uma quantidade de tempo igual para utilizar a CPU.

Após o término do seu time slice, o processo retorna para a fila e o próximo processo recebe acesso à CPU.

Esse ciclo continua até que todos os processos sejam concluídos.

---

## ⭐ Escalonamento por Prioridade

Os processos recebem diferentes níveis de prioridade.

Processos com maior prioridade podem receber acesso à CPU antes dos processos de menor prioridade.

---

# 🐌 Desempenho do Computador

Quando o computador está lento, uma das possíveis causas é a existência de muitos processos competindo pelos recursos do sistema.

Também pode ocorrer de um único processo consumir uma quantidade excessiva de recursos.

Entre os recursos que podem ser sobrecarregados estão:

- 🧠 Memória RAM;
- ⚙️ CPU;
- 💽 Armazenamento.

O sistema operacional utiliza o gerenciamento de processos para distribuir os recursos e manter o computador funcionando de maneira eficiente.

---

# 📌 Resumo

Um processo é um programa em execução.

O kernel é responsável por gerenciar os processos e distribuir recursos limitados, como CPU e memória RAM.

Para permitir que vários processos funcionem, o sistema operacional utiliza:

- ⏱️ Time slices;
- 📅 Algoritmos de escalonamento;
- ⭐ Prioridades;
- 🔄 Alternância entre processos.

Entre os algoritmos de escalonamento estudados estão:

- 📥 FIFO;
- 🔄 Round Robin;
- ⭐ Escalonamento por Prioridade.

O gerenciamento de processos permite que o computador execute vários programas de forma eficiente, mantendo o sistema responsivo e garantindo que os recursos sejam compartilhados entre os processos.
