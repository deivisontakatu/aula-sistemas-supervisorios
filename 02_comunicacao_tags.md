# Comunicação e Tags em SCADA

## 🎯 Objetivo  
Entender como os dados são estruturados e comunicados em sistemas SCADA, incluindo a organização em tags e o uso de protocolos industriais para integração com CLPs.

---

## 📚 Conceitos-chave  
- Tags (variáveis)  
- Tipos de dados (digital, analógico)  
- Endereçamento de memória  
- Drivers de comunicação  
- Protocolos industriais  
  - Modbus (RTU/TCP)  
  - OPC  
  - OPC UA  
  - Ethernet/IP  
- Comunicação SCADA ↔ PLC  
- Leitura e escrita de dados  
- Tempo de varredura (scan time)  
- Sincronização de dados  

---

## 🧠 Explicação  

Em sistemas SCADA, os dados do processo industrial são representados por **tags**.  
Uma tag é uma variável que representa um ponto do processo, como temperatura, nível ou estado de um motor.

---

### 🏷️ Tags (variáveis)

As tags são a base do SCADA. Elas funcionam como uma ponte entre o mundo físico e o sistema digital.

Exemplos:
- `Temperatura_Tanque`  
- `Nivel_Reservatorio`  
- `Motor_Ligado`  

Cada tag possui:
- Nome  
- Tipo de dado  
- Endereço no CLP  
- Valor atual  

---

### 🔢 Tipos de dados

Os principais tipos de dados são:

- **Booleano (BOOL):**
  - Verdadeiro ou falso  
  - Ex: Motor ligado/desligado  

- **Inteiro (INT):**
  - Números inteiros  
  - Ex: contador de peças  

- **Real (FLOAT):**
  - Números com casas decimais  
  - Ex: temperatura  

---

### 📡 Comunicação com CLP

O SCADA não acessa sensores diretamente. Ele se comunica com o CLP.

Fluxo:
Sensor → CLP → SCADA

O SCADA:
- Lê valores do CLP  
- Envia comandos para o CLP  

---

### 🔌 Drivers de comunicação

Drivers são responsáveis por conectar o SCADA aos dispositivos.

Funções:
- Traduzir protocolos  
- Gerenciar conexões  
- Ler/escrever dados  

Exemplo:
- Driver Modbus  
- Driver OPC  

---

### 🌐 Protocolos industriais

#### Modbus
- Simples e muito usado  
- Pode ser:
  - RTU (serial)  
  - TCP (rede)  

#### OPC (OLE for Process Control)
- Padrão para comunicação industrial  
- Permite integração entre sistemas  

#### OPC UA
- Versão moderna do OPC  
- Mais segura  
- Baseada em rede  

#### Ethernet/IP
- Usado em redes industriais Ethernet  
- Alta velocidade  

---

### 🔁 Leitura e escrita de dados

O SCADA realiza dois tipos de operação:

- **Leitura (Read):**
  - Obtém dados do CLP  

- **Escrita (Write):**
  - Envia comandos para o CLP  

Exemplo:
- Leitura: nível do tanque  
- Escrita: ligar bomba  

---

### ⏱️ Tempo de varredura (Scan Time)

É o tempo que o SCADA leva para atualizar os dados.

- Quanto menor, mais rápido  
- Quanto maior, menor carga no sistema  

---

### 🧩 Organização dos dados

Os dados são organizados em:
- Tags  
- Grupos de tags  
- Estruturas  

Isso facilita:
- Manutenção  
- Leitura  
- Escalabilidade  

---

## 🔧 Ferramentas relacionadas  

### 🛠️ Kepware
- Servidor OPC  
- Integra diversos protocolos  

### 🛠️ OPC Server
- Intermediário entre SCADA e dispositivos  
- Padroniza comunicação  

---

## 💻 Exemplo prático  

### 🎯 Criando tags simuladas

Exemplo de tags:


Nivel_Tanque = 80.5
Temperatura = 35.2
Motor = TRUE


---

### 🔗 Simulação de conexão

Passos:

1. Criar tag no SCADA  
2. Definir tipo de dado  
3. Associar endereço do CLP  
4. Configurar driver  
5. Testar leitura  

---

### 📊 Exemplo de mapeamento


Tag: Nivel_Tanque
Tipo: FLOAT
Endereço: %MW100


---

### 🔄 Fluxo completo


Sensor → CLP (%MW100) → Driver → SCADA Tag → Tela


---

## ⚠️ Erros comuns  

- Criar tags sem padrão de nome  
- Usar tipo de dado errado  
- Configurar endereço incorreto  
- Ignorar protocolo correto  
- Não configurar driver corretamente  
- Não testar comunicação  
- Confundir OPC com protocolo físico  
- Usar scan time inadequado  

---

## 📝 Resumo  

- Tags representam variáveis do processo  
- SCADA não acessa sensor diretamente  
- Comunicação é feita via CLP  
- Drivers conectam SCADA aos dispositivos  
- Protocolos comuns:
  - Modbus  
  - OPC  
  - Ethernet/IP  
- SCADA:
  - Lê dados  
  - Escreve comandos  

---

## 📖 Referências  

- BOYER, Stuart A. *SCADA: Supervisory Control and Data Acquisition*. ISA, 2009.  
- RODRÍGUEZ PENÍN, Aquilino. *Sistemas SCADA: guía práctica*. Marcombo, 2007.  
- GARCIA JUNIOR, Ervaldo. *Introdução a sistemas de supervisão, controle e aquisição de dados*. 2019.  
- PETRUZZELLA, F. D. *Controladores Lógicos Programáveis*. 2014.  

---

## 🚀 Desafio / Exercício  

### 🧠 Exercício 1
Crie 5 tags para um sistema de tanque:
- Nível  
- Temperatura  
- Pressão  
- Bomba  
- Válvula  

---

### 🧠 Exercício 2
Defina:
- Tipo de dado  
- Nome da tag  
- Função  

---

### 🧠 Exercício 3
Explique o fluxo:


Sensor → CLP → SCADA


---

### 🧠 Exercício 4
Qual a diferença entre:
- Modbus  
- OPC  

---

### 🧠 Exercício 5
Explique o que é um driver de comunicação.

---

### 🧠 Exercício 6
Dê um exemplo de leitura e escrita no SCADA.

---

### 🧠 Exercício 7
Explique o que acontece se o endereço da tag estiver errado.

---

### 🧠 Exercício 8
Explique o conceito de scan time.

---

### 🧠 Exercício 9
Cite dois protocolos industriais.

---

### 🧠 Exercício 10
Descreva como o SCADA se conecta a um CLP.

---

## 🧩 Expansão do conteúdo  

- Segurança na comunicação  
- Redes industriais  
- Diagnóstico de falhas  
- Latência de comunicação  
- Redundância  

---

## 📌 Observação final  

A comunicação é uma das partes mais críticas do SCADA.  
Se ela falhar, todo o sistema perde funcionalidade.  

Dominar tags e protocolos é essencial para qualquer profissional da área.

---