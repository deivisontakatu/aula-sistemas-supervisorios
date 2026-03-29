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

## 🧩 2. Tags e Drivers de Comunicação

### 🔖 Tags

Tags são **variáveis internas do sistema** que representam dados do processo.

### 📌 Tipos de tags:

* **Digitais** → 0 ou 1 (ligado/desligado)
* **Analógicas** → valores contínuos (ex: 75°C)

---

### 💡 Exemplo

```text
Nivel_Tanque = 80%
Motor_Bomba = ON
```

---

### 🔌 Drivers de Comunicação

São responsáveis por **conectar o SCADA aos dispositivos de campo**.

### 📡 Protocolos comuns:

* Modbus
* OPC
* Profibus
* Ethernet/IP

---

### 💡 Exemplo real

SCADA ↔ Driver Modbus ↔ CLP ↔ Sensor

---

### 📚 Dica de estudo

👉 Se cair na prova:

* **Tag = dado**
* **Driver = comunicação**

---

## 🖥️ 3. Telas, Objetos de Animação e Scripts

### 🖼️ Telas (IHM)

São as **interfaces gráficas** do sistema.

Permitem:

* visualizar o processo
* interagir com o sistema

---

### 💡 Exemplo

Tela mostrando:

* tanque com nível animado
* botão ligar/desligar bomba

---

### 🎨 Objetos de Animação

Elementos que mudam dinamicamente:

* cores (verde = ligado, vermelho = desligado)
* gráficos
* barras de nível

---

### 📜 Scripts

Permitem adicionar lógica personalizada.

### 💡 Exemplo:

```pseudo
IF nivel > 90 THEN
  desligar bomba
END IF
```

---

### 📚 Dica de estudo

👉 Pense:

* Tela = visual
* Animação = dinâmica
* Script = lógica

---

## 📊 4. Históricos e Relatórios

### 📈 Históricos

Armazenam dados ao longo do tempo.

Permitem:

* análise de desempenho
* identificação de falhas
* auditoria

---

### 💡 Exemplo

Gráfico mostrando temperatura nas últimas 24h

---

### 📄 Relatórios

Organizam dados em formato estruturado.

Podem conter:

* consumo
* produção
* falhas

---

### 📚 Dica de estudo

👉 Diferença clássica de prova:

* **Histórico = dado bruto ao longo do tempo**
* **Relatório = informação organizada**

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

### 📚 Dica de estudo

👉 Palavras-chave de prova:

* autenticação
* autorização
* controle de acesso

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
