# 🌐 Roteadores

## 🎯 Objetivos

Neste conteúdo, aprendemos sobre os **roteadores**, dispositivos responsáveis por conectar diferentes redes e permitir a comunicação entre elas.

Também vimos:

- O que é um roteador;
- A diferença entre Hub, Switch e Roteador;
- Em qual camada do modelo OSI cada dispositivo opera;
- Como os roteadores encaminham os pacotes de dados;
- O que são tabelas de roteamento;
- Como funciona o protocolo BGP;
- A diferença entre roteadores domésticos e roteadores de provedores de Internet (ISP);
- Como os dados percorrem a Internet.

---

# 🌍 Introdução

Até agora vimos que:

- 🔌 **Cabos** conectam dispositivos fisicamente;
- 🔀 **Switches** conectam dispositivos dentro da mesma rede local (LAN).

Mas surge uma pergunta:

**Como um computador da sua casa consegue se comunicar com um servidor localizado em outro país?**

A resposta está nos **roteadores**.

Os roteadores são responsáveis por conectar diferentes redes e encaminhar os pacotes de dados até o destino correto.

---

# 🛣️ O que é um Roteador?

Um **roteador (Router)** é um dispositivo de rede responsável por encaminhar pacotes de dados entre redes diferentes.

Enquanto um switch conecta dispositivos dentro da mesma rede local (LAN), o roteador conecta redes independentes.

Por exemplo:

```text
Rede da sua casa
        │
     Roteador
        │
──────── Internet ────────
        │
Servidor de um site
```

Sem os roteadores, seria impossível acessar sites, enviar e-mails ou utilizar praticamente qualquer serviço disponível na Internet.

---

# 📚 Camadas do Modelo OSI

Cada dispositivo de rede atua em uma camada diferente do Modelo OSI.

| Dispositivo | Camada OSI | Função |
|-------------|------------|--------|
| 🔌 Hub | Camada 1 - Física | Repete os sinais elétricos |
| 🔀 Switch | Camada 2 - Enlace | Encaminha quadros Ethernet |
| 🌐 Roteador | Camada 3 - Rede | Encaminha pacotes IP entre redes |

O roteador trabalha analisando os **endereços IP** dos pacotes para decidir o melhor caminho até o destino.

---

# 📦 Como Funciona um Roteador?

Sempre que um computador envia dados para outra rede, o roteador recebe esse pacote.

Ele analisa:

- 📍 O endereço IP de origem;
- 🎯 O endereço IP de destino.

Depois disso, consulta sua **tabela de roteamento** para decidir por qual caminho o pacote deverá seguir.

O objetivo é encontrar a melhor rota disponível até o destino.

---

# 🗺️ Tabela de Roteamento

Todo roteador possui uma **tabela de roteamento**.

Essa tabela funciona como um mapa da rede.

Ela informa:

- Quais redes o roteador conhece;
- Qual caminho utilizar para cada destino;
- Qual é o próximo roteador para encaminhar os dados.

Sempre que um pacote chega ao roteador, ele consulta essa tabela antes de encaminhá-lo.

---

# 🏠 Roteadores Domésticos

Os roteadores utilizados em residências ou pequenos escritórios possuem tabelas de roteamento relativamente simples.

Normalmente eles conhecem apenas:

- Sua rede local (LAN);
- O caminho até o provedor de Internet (ISP).

Exemplo:

```text
Notebook
      │
Smartphone
      │
Smart TV
      │
   🌐 Roteador
      │
      ▼
     ISP
```

Quando um dispositivo deseja acessar um site, o roteador envia os pacotes para o provedor de Internet.

---

# 🏢 Roteadores dos ISPs

Os roteadores utilizados pelos provedores de Internet são muito mais complexos.

Eles precisam conectar:

- Milhares de clientes;
- Diversos roteadores;
- Outras redes;
- Outros provedores;
- Data centers;
- Grandes empresas.

Esses roteadores possuem tabelas de roteamento muito maiores e precisam decidir constantemente quais são as melhores rotas para encaminhar os dados.

---

# 🌍 Como os Dados Percorrem a Internet?

Quando você acessa um site, o pacote normalmente passa por vários roteadores até chegar ao servidor.

Um exemplo simplificado seria:

```text
💻 Seu computador
        │
🌐 Roteador da casa
        │
🏢 ISP local
        │
🌎 Backbone da Internet
        │
🏢 ISP do servidor
        │
🖥️ Servidor do site
```

Na prática, um pacote pode passar por dezenas de roteadores antes de chegar ao seu destino.

Cada roteador analisa o endereço IP e decide qual será o próximo passo da viagem.

---

# 📡 O Protocolo BGP

Os grandes roteadores da Internet utilizam um protocolo chamado **BGP (Border Gateway Protocol)**.

O BGP é responsável por compartilhar informações sobre as rotas disponíveis entre diferentes redes independentes.

Graças ao BGP, os roteadores conseguem descobrir:

- Quais caminhos existem;
- Qual caminho é mais rápido;
- Qual rota está disponível;
- Como evitar rotas indisponíveis.

---

# ⚙️ Como Funciona o BGP?

Imagine que existam vários caminhos possíveis para chegar a um servidor.

O BGP permite que os roteadores troquem informações sobre essas rotas e escolham a mais adequada.

Ele ajuda os roteadores a:

- 📍 Aprender novas rotas;
- 🚦 Escolher o melhor caminho;
- 🔄 Atualizar rotas quando houver mudanças;
- 🌐 Encaminhar corretamente o tráfego entre diferentes redes.

Esse protocolo é um dos pilares do funcionamento da Internet.

---

# 🆚 Comparando Hub, Switch e Roteador

| Característica | 🔌 Hub | 🔀 Switch | 🌐 Roteador |
|----------------|---------|-----------|-------------|
| Camada OSI | 1 | 2 | 3 |
| Analisa dados | ❌ Não | ✅ Ethernet | ✅ Endereços IP |
| Conecta | Dispositivos | Dispositivos | Redes |
| Inteligência | Baixa | Média | Alta |
| Encaminhamento | Todas as portas | Porta correta | Melhor rota entre redes |

---

# 🏠 Exemplo Prático

Imagine que você deseja acessar um vídeo no YouTube.

O caminho pode ser:

```text
Notebook
      │
Switch
      │
Roteador doméstico
      │
ISP
      │
Vários roteadores da Internet
      │
Servidor do YouTube
```

Cada roteador verifica o endereço IP do destino e encaminha o pacote até que ele chegue ao servidor correto.

---

# 💡 Curiosidade

Quando acessamos um site localizado em outro continente, os dados podem atravessar diversos países.

Mesmo assim, o processo normalmente acontece em poucos milissegundos graças ao trabalho conjunto dos roteadores espalhados pela Internet.

---

# 📚 Principais Conceitos

- 🌐 O roteador conecta redes diferentes.
- 📦 Os roteadores trabalham com endereços IP.
- 🛣️ Eles encaminham os pacotes pela melhor rota disponível.
- 🗺️ Todo roteador possui uma tabela de roteamento.
- 🏠 Roteadores domésticos possuem tabelas simples.
- 🏢 Roteadores dos ISPs possuem tabelas muito maiores e mais complexas.
- 🌍 Um pacote pode atravessar dezenas de roteadores até chegar ao destino.
- 📡 O protocolo BGP permite que roteadores compartilhem informações sobre rotas e escolham os melhores caminhos para encaminhar o tráfego.

---

# 🎯 Resumo

Os roteadores são dispositivos fundamentais para o funcionamento da Internet. Eles operam na **Camada de Rede (Layer 3)** do modelo OSI e utilizam os endereços IP para encaminhar pacotes entre redes diferentes.

Para decidir o caminho mais adequado, os roteadores consultam suas tabelas de roteamento. Em grandes redes, como as dos provedores de Internet, o **Border Gateway Protocol (BGP)** permite que diferentes roteadores compartilhem informações sobre rotas, tornando possível escolher os caminhos mais eficientes para o tráfego de dados.

---

# ✅ Conclusão

Os roteadores são responsáveis por interligar redes e garantir que os pacotes de dados cheguem ao destino correto, mesmo quando precisam atravessar diversos países e provedores de Internet.

Compreender seu funcionamento, a importância das tabelas de roteamento e o papel do protocolo **BGP** é essencial para entender como a Internet funciona e para atuar em áreas de redes, infraestrutura e suporte técnico.
