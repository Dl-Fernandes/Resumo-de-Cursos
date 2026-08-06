# 🔀 Hubs e Switches

## 🎯 Objetivos

Neste conteúdo, aprendemos sobre dois dos principais dispositivos utilizados em redes de computadores: **Hub** e **Switch**.

Também vimos:

- O que são hubs e switches;
- Como eles conectam dispositivos em uma rede;
- As diferenças entre comunicação ponto a ponto e comunicação compartilhada;
- O conceito de domínio de colisão;
- Como ocorrem as colisões de dados;
- As vantagens do switch em relação ao hub;
- O impacto desses dispositivos no desempenho da rede.

---

# 🌐 Introdução

Para que computadores e outros dispositivos possam trocar informações, eles precisam estar conectados por um meio físico e por equipamentos responsáveis por distribuir os dados.

Embora um cabo de rede possa conectar diretamente dois computadores, redes com vários dispositivos necessitam de equipamentos capazes de interligar todas essas conexões.

Os dois dispositivos mais básicos para essa finalidade são:

- 🔌 Hub;
- 🔀 Switch.

Embora ambos tenham a função de conectar dispositivos, seu funcionamento é bastante diferente.

---

# 🔌 Comunicação Ponto a Ponto

A forma mais simples de comunicação é utilizando apenas um cabo de rede.

Nesse caso:

```text
💻 ───────────── 💻
```

Esse tipo de conexão é chamado de **ponto a ponto**, pois conecta apenas dois dispositivos diretamente.

Quando há necessidade de conectar vários computadores, é necessário utilizar um equipamento intermediário.

---

# 🔌 Hub

O **Hub** é um dispositivo de rede que opera na **Camada Física (Layer 1)** do modelo OSI.

Sua principal função é conectar diversos dispositivos utilizando várias portas Ethernet.

Um exemplo simples seria:

```text
        💻
         │
💻 ─── HUB ─── 💻
         │
        💻
```

---

# ⚙️ Como Funciona um Hub?

O Hub **não interpreta os dados** que recebe.

Sempre que um computador envia uma informação, o Hub simplesmente **repete esse sinal para todas as portas conectadas**.

Ou seja:

- O computador A envia um pacote;
- O Hub recebe o pacote;
- O Hub envia esse mesmo pacote para todos os computadores.

Cada computador recebe os dados e verifica se é realmente o destinatário.

Se não for, simplesmente descarta o pacote.

---

# ❌ Desvantagens do Hub

Como todos recebem todas as transmissões, surgem alguns problemas:

- Grande quantidade de tráfego desnecessário;
- Compartilhamento da largura de banda;
- Baixa eficiência;
- Redução do desempenho;
- Maior número de colisões.

Por esse motivo, atualmente os hubs praticamente não são mais utilizados.

---

# 💥 Colisão de Dados

Uma **colisão** acontece quando dois ou mais dispositivos tentam transmitir dados ao mesmo tempo utilizando o mesmo meio físico.

Exemplo:

```text
PC A  ─────►
             HUB
PC B  ─────►
```

Os sinais chegam simultaneamente e acabam se misturando.

Como consequência:

- Os dados podem ser corrompidos;
- É necessário retransmitir os pacotes;
- A comunicação fica mais lenta.

Quanto maior o número de computadores conectados ao Hub, maior será a chance de ocorrerem colisões.

---

# 🌐 Domínio de Colisão

Um **domínio de colisão** é uma área da rede onde apenas um dispositivo pode transmitir dados por vez.

Se dois ou mais dispositivos enviarem informações simultaneamente dentro do mesmo domínio, ocorre uma colisão.

### No Hub

Todos os computadores compartilham o mesmo domínio de colisão.

```text
💻
 │
💻── HUB ──💻
 │
💻

Domínio de colisão único
```

Isso significa que apenas um dispositivo pode transmitir por vez.

Quanto maior a quantidade de dispositivos conectados, maior a probabilidade de colisões.

---

# 🔀 Switch

O **Switch** é um dispositivo que opera na **Camada de Enlace (Layer 2)** do modelo OSI.

Assim como o Hub, ele conecta diversos dispositivos.

Entretanto, seu funcionamento é muito mais inteligente.

```text
        💻
         │
💻 ─ Switch ─ 💻
         │
        💻
```

---

# ⚙️ Como Funciona um Switch?

O Switch analisa os dados recebidos antes de encaminhá-los.

Ele identifica qual é o dispositivo destinatário e envia os dados **somente para a porta correta**.

Exemplo:

```text
PC A envia dados para PC C

PC A
 │
 ▼
Switch
 │
 ▼
PC C
```

Os demais computadores nem chegam a receber esse pacote.

---

# ✅ Vantagens do Switch

Como o Switch envia dados apenas para o destinatário correto, ele oferece diversas vantagens:

- 🚀 Maior velocidade;
- 📈 Melhor desempenho;
- 🔒 Comunicação mais eficiente;
- 📦 Menor tráfego desnecessário;
- 💥 Redução ou eliminação das colisões;
- 📡 Melhor aproveitamento da largura de banda.

---

# 🔄 Hub x Switch

| Característica | 🔌 Hub | 🔀 Switch |
|---------------|---------|-----------|
| Camada do OSI | Camada Física (Layer 1) | Camada de Enlace (Layer 2) |
| Analisa os dados | ❌ Não | ✅ Sim |
| Envia dados para | Todos os dispositivos | Apenas o destinatário |
| Colisões | Muitas | Poucas ou inexistentes |
| Desempenho | Baixo | Alto |
| Eficiência | Menor | Maior |

---

# 🏢 Exemplo Prático

Imagine uma empresa com 20 computadores.

### Utilizando um Hub

Sempre que um computador envia um arquivo:

- Os outros 19 computadores recebem esse pacote;
- Cada computador precisa verificar se o pacote é destinado a ele;
- O tráfego aumenta;
- O risco de colisões é elevado.

---

### Utilizando um Switch

Quando um computador envia um arquivo:

- O Switch identifica o destinatário;
- Apenas o computador correto recebe os dados;
- Os demais dispositivos continuam livres para transmitir;
- A rede permanece rápida e organizada.

---

# 💡 Por que o Switch é Melhor?

O Switch consegue manter uma comunicação muito mais eficiente porque reduz significativamente o domínio de colisão.

Na prática:

- Cada porta do Switch funciona praticamente como um domínio de colisão independente.
- Isso permite que vários dispositivos transmitam dados ao mesmo tempo sem interferência entre si.

Esse comportamento melhora o desempenho da rede e torna a comunicação muito mais confiável.

---

# 📚 Principais Conceitos

- 🔌 Cabos permitem conexões ponto a ponto entre dois dispositivos.
- 🔌 O Hub conecta vários dispositivos, mas envia todos os dados para todas as portas.
- 💥 Colisões acontecem quando dois ou mais dispositivos transmitem ao mesmo tempo.
- 🌐 Um domínio de colisão é uma área da rede onde apenas um dispositivo pode transmitir por vez.
- 🔀 O Switch opera na Camada de Enlace (Layer 2).
- 📦 O Switch analisa os dados antes de encaminhá-los.
- 📡 O Switch envia os dados apenas para o destinatário correto.
- 🚀 O uso de switches melhora significativamente o desempenho da rede.

---

# 🎯 Resumo

Os hubs e os switches são dispositivos utilizados para conectar computadores em uma rede local. Enquanto o Hub simplesmente replica todos os dados recebidos para todas as portas, o Switch identifica o destinatário da comunicação e encaminha os dados apenas para o dispositivo correto.

Essa diferença faz com que os switches reduzam drasticamente as colisões, utilizem melhor a largura de banda e ofereçam maior velocidade, estabilidade e eficiência na comunicação entre dispositivos.

---

# ✅ Conclusão

Embora o Hub tenha sido um equipamento importante nas primeiras redes locais, atualmente ele foi praticamente substituído pelo Switch devido ao seu melhor desempenho.

O Switch tornou-se um dos dispositivos mais importantes das redes modernas, permitindo comunicações rápidas, organizadas e confiáveis entre computadores, servidores e demais equipamentos conectados à rede.
