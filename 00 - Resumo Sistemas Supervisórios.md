# 🖥️ Guia Completo — Sistemas Supervisórios SCADA (6 Tópicos)

---

## 📌 1. Introdução e Aplicativos

Os sistemas **SCADA (Supervisory Control and Data Acquisition)** são utilizados para **monitorar, supervisionar e controlar processos industriais em tempo real**.

Eles fazem a ponte entre:

* o **mundo físico** (sensores, CLPs)
* e o **operador humano** (interface gráfica)

### 🎯 Funções principais

* Coletar dados (nível, temperatura, pressão)
* Exibir informações em tempo real
* Permitir controle remoto (ligar/desligar equipamentos)
* Gerar alarmes

---

### 🌍 Aplicações reais

* 🏭 Indústrias → controle de produção
* ⚡ Energia → monitoramento de subestações
* 🚰 Saneamento → controle de nível de reservatórios
* ⛽ Petróleo e gás → monitoramento de dutos

---

### 💡 Exemplo prático

Um sistema SCADA pode:

* mostrar o nível de um tanque
* abrir automaticamente uma válvula
* disparar um alarme se o nível estiver crítico

---

### 📚 Dica de estudo

👉 Sempre pense:

> “SCADA = supervisão + visualização + controle”

---

# 🧩 2. Tags e Drivers de Comunicação (Detalhado)

## 🔖 TAGS (Variáveis do SCADA)

Tags são **representações digitais das variáveis do processo físico** dentro do sistema SCADA.

### 🎯 Função das Tags
- Conectar o mundo físico ao sistema digital
- Permitir leitura e escrita de dados
- Servir como base para:
  - Telas (IHM)
  - Alarmes
  - Históricos
  - Scripts

---

## 📌 Tipos de Tags

### 🔘 1. Digitais (Booleanas)
- Valores: 0 ou 1 (OFF/ON)
- Representam estados

**Exemplos:**
- `Motor_Bomba = 1` → ligado
- `Alarme_Nivel_Alto = 0` → desativado
- `Valvula_Aberta = 1`

**Uso prático:**
- Botões (liga/desliga)
- Indicadores (LEDs)
- Alarmes

---

### 📊 2. Analógicas (Contínuas)
- Valores numéricos (inteiros ou reais)

**Exemplos:**
- `Nivel_Tanque = 80%`
- `Temperatura = 75.5°C`
- `Pressao = 3.2 bar`

**Uso prático:**
- Gráficos
- Medidores (gauges)
- Controle automático

---

### 🧠 3. Tags Internas (Soft Tags)
- Não vêm de sensores reais
- Criadas dentro do SCADA

**Exemplos:**
- `Setpoint_Temperatura = 70`
- `Tempo_Bomba_Ligada`
- `Media_Diaria_Nivel`

---

### 🔄 4. Tags de Escrita (Output)
- Enviam comandos para o processo

**Exemplos:**
- `Liga_Bomba = 1`
- `Abrir_Valvula = 0`

---

## 🔌 DRIVERS DE COMUNICAÇÃO

Drivers são responsáveis por:
- Fazer a **comunicação entre SCADA e dispositivos**
- Traduzir protocolos industriais
- Ler e escrever tags nos equipamentos

---

## 📡 Protocolos de Comunicação (Detalhado)

### 🔷 1. Modbus

**Tipo:** Mestre/Escravo (Master/Slave)  
**Uso:** Muito comum e simples  

**Funcionamento:**
- SCADA (Master) solicita dados
- Dispositivo (Slave) responde

**Exemplo prático:**
- SCADA pede: "Qual o nível do tanque?"
- CLP responde: "80"

**Características:**
- Pode ser:
  - Modbus RTU (serial)
  - Modbus TCP (rede Ethernet)
- Usa registradores:
  - Coil → digital (0/1)
  - Holding Register → analógico

**Quando usar:**
- Sistemas simples
- Integração com CLPs básicos
- Projetos acadêmicos

---

### 🔷 2. OPC (OLE for Process Control)

**Tipo:** Cliente/Servidor  

**Funcionamento:**
- OPC Server → conecta com dispositivos
- SCADA (Client) → lê dados do servidor

**Exemplo:**
- CLP → OPC Server → SCADA

**Vantagens:**
- Padronização
- Integra vários protocolos
- Facilita integração

**Tipos:**
- OPC DA (antigo)
- OPC UA (moderno, seguro)

**Quando usar:**
- Integração com múltiplos equipamentos
- Sistemas complexos
- Indústria moderna

---

### 🔷 3. Profibus

**Tipo:** Rede industrial de alta velocidade  

**Funcionamento:**
- Comunicação entre vários dispositivos em barramento

**Exemplo:**
- CLP Siemens ↔ sensores ↔ atuadores

**Características:**
- Muito rápido
- Alta confiabilidade
- Muito usado na Europa

**Quando usar:**
- Sistemas industriais robustos
- Automação pesada
- Equipamentos Siemens

---

### 🔷 4. Ethernet/IP

**Tipo:** Rede industrial baseada em Ethernet  

**Funcionamento:**
- Comunicação via rede (TCP/IP)

**Exemplo:**
- SCADA ↔ CLP Allen-Bradley ↔ sensores

**Características:**
- Alta velocidade
- Comunicação em tempo real
- Usa infraestrutura de rede comum

**Quando usar:**
- Indústria moderna
- Integração com TI (redes)
- Sistemas distribuídos

---

## 🔁 Relação TAG + DRIVER

Exemplo completo:

Sensor → CLP → Driver (Modbus) → SCADA → Tag

**Fluxo real:**
- Sensor mede nível (80%)
- CLP armazena valor
- Driver Modbus lê o dado
- SCADA atualiza a tag `Nivel_Tanque`

- **Tags = dados do processo**
- **Drivers = comunicação**
- **Protocolos = linguagem da comunicação**

👉 Sem driver → SCADA não "enxerga" o processo  
👉 Sem tags → SCADA não tem o que mostrar/controlar

---

# 🖥️ 3. Telas, Objetos de Animação e Scripts (SCADA)

## 🖼️ Telas (IHM - Interface Homem-Máquina)
São as interfaces gráficas que permitem interação entre operador e processo.

### 🎯 Funções
- Monitorar variáveis em tempo real
- Controlar equipamentos (botões, sliders)
- Exibir alarmes e eventos
- Navegar entre processos

### 🧩 Tipos de telas
- **Overview (geral):** visão completa do sistema
- **Processo:** detalhamento (ex: tanque, bomba)
- **Alarmes:** lista de falhas
- **Histórico:** gráficos e tendências

---

## 🎨 Objetos de Animação
Elementos visuais conectados às **tags** que mudam dinamicamente.

### 🔧 Tipos principais

#### 🎨 Cor (status)
- Verde = ligado
- Vermelho = desligado
- Amarelo = alerta

#### 📏 Nível / escala
- Barras que sobem/descem conforme valor
- Ex: nível do tanque

#### 🔄 Rotação
- Representa movimento
- Ex: bomba girando quando ligada

#### 👁️ Visibilidade
- Mostrar/esconder objetos
- Ex: alarme aparece quando ativo

#### 🔢 Texto dinâmico
- Exibe valores em tempo real
- Ex: "Temp: 75°C"

---

## 📜 Scripts (Lógica)
Permitem implementar regras e automações no SCADA.

### 🎯 Usos
- Controle automático
- Segurança (intertravamento)
- Alarmes inteligentes
- Cálculos e temporização

---

## 💡 Exemplos

### ⚙️ Controle automático
```pseudo
IF nivel < 20 THEN
  ligar_bomba
END IF
````

### 🚨 Alarme

```pseudo
IF nivel > 90 THEN
  desligar_bomba
  ativar_alarme
END IF
```

### 🔒 Segurança

```pseudo
IF valvula_fechada THEN
  bloquear_bomba
END IF
```

### ⏱️ Temporização

```pseudo
IF bomba_ligada THEN
  tempo = tempo + 1
END IF
```

### 📊 Cálculo

```pseudo
media = (temp1 + temp2) / 2
```

---

## 🔗 Integração

Fluxo do sistema:

TAG → SCRIPT → ANIMAÇÃO → TELA

### ✔ Exemplo prático

* Tag: `Nivel_Tanque = 95`
* Script: desliga bomba
* Animação: tanque fica vermelho
* Tela: mostra alerta

---
# 📊 4. Históricos e Relatórios (SCADA)

## 📈 Históricos
São registros contínuos das **tags ao longo do tempo**.

### 🎯 Para que servem
- Analisar comportamento do processo
- Detectar falhas e anomalias
- Fazer auditoria e rastreabilidade
- Apoiar decisões operacionais

### 🧩 Tipos de históricos
- **Tendência (Trend):** gráfico contínuo (tempo × valor)
- **Eventos:** registro de mudanças (ON/OFF, alarmes)
- **Batch/Lote:** dados por processo específico

### ⚙️ Como funcionam
- SCADA coleta dados das tags
- Armazena em banco (SQL, histórico interno)
- Frequência de coleta:
  - Por tempo (ex: a cada 1s)
  - Por evento (quando muda valor)

### 💡 Exemplos
- Temperatura registrada a cada 1 min → análise de aquecimento
- Registro de liga/desliga da bomba → tempo de uso
- Nível do tanque → detectar consumo irregular

### 📌 Exemplo prático
Gráfico de 24h:
- 08:00 → 25°C
- 12:00 → 40°C
- 18:00 → 35°C

👉 Permite identificar picos e padrões

---

## 📄 Relatórios
São dados **organizados e resumidos** a partir dos históricos.

### 🎯 Para que servem
- Apresentar resultados
- Apoiar gestão
- Documentar operação
- Cumprir normas/auditorias

### 🧩 Tipos de relatórios
- **Produção:** quantidade produzida por período
- **Consumo:** energia, água, matéria-prima
- **Falhas:** alarmes e paradas
- **Eficiência:** tempo ativo vs parado

### ⚙️ Características
- Gerados automaticamente (diário, semanal)
- Formato estruturado (tabelas, PDF, Excel)
- Baseados em dados históricos

### 💡 Exemplos
- Consumo de água: 1200L/dia
- Tempo da bomba ligada: 6h/dia
- Número de falhas: 3 ocorrências

### 📌 Exemplo prático
Relatório diário:
- Produção: 500 unidades
- Falhas: 2 alarmes
- Tempo parado: 30 min

---

## 🔁 Relação entre eles

Histórico → dado bruto (tempo real)  
Relatório → dado processado (resumo)

---


## 🔐 5. Senhas e Segurança

Controle de acesso ao sistema.

### 👥 Níveis de usuário:

* Operador → visualiza e controla
* Supervisor → altera parâmetros
* Administrador → configura sistema

---

### 🎯 Objetivos

* evitar acessos indevidos
* proteger dados
* garantir segurança operacional

---

### 💡 Exemplo

Operador não pode alterar configurações críticas

---

## 🛠️ 6. Exemplos e Desenvolvimento de um Sistema SCADA

### 🧪 Etapas de desenvolvimento

1. Levantamento de requisitos
2. Definição de tags
3. Configuração de comunicação
4. Criação de telas
5. Implementação de scripts
6. Testes

---

### 💡 Exemplo completo (clássico de prova)

Sistema de tanque:

* Sensor mede nível
* SCADA mostra nível na tela
* Se nível > 90% → alarme
* Se nível < 20% → liga bomba

---

## 💻 Softwares SCADA para estudar

  ### 🧪 Para prática (recomendado)

  * **Elipse E3**
    👉 Muito usado no Brasil (excelente pra prova)

  * **FactoryTalk View**
    👉 Muito usado em indústria

  * **WinCC**
    👉 Padrão industrial (Siemens)

  ---

  ### 🆓 Gratuitos / estudo

  * **ScadaBR**
    👉 Open source (ótimo pra aprender)

  * **Ignition**
    👉 Versão trial completa

---

## 🎯 Dicas finais para prova

* SCADA ≠ CLP
  → SCADA supervisiona, CLP controla

* Tags = variáveis do processo

* Drivers = comunicação

* IHM = interface visual

* Histórico ≠ relatório

---

## 🧠 Síntese Final

* SCADA monitora e controla processos industriais
* Integra dados, interface e automação
* Utiliza tags, drivers e telas
* Armazena dados e gera relatórios
* Possui controle de acesso
* Pode ser desenvolvido com diferentes softwares

---
