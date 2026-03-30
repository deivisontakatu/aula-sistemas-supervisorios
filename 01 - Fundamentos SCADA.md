# Fundamentos de SCADA

## 🎯 Objetivo  
Compreender o que são sistemas SCADA e sua aplicação na automação industrial, entendendo sua importância no monitoramento e supervisão de processos industriais modernos.

---

## 📚 Conceitos-chave  
- SCADA  
- IHM  
- Aplicativos SCADA  
- Arquitetura (campo, controle, supervisão)  
- Integração com CLP  
- Sistemas centralizados  
- Sistemas distribuídos  
- Supervisão de processos  
- Aquisição de dados  
- Automação industrial  
- Tempo real  
- Sistemas industriais  

---

## 🧠 Explicação  

Os sistemas SCADA (Supervisory Control and Data Acquisition) são plataformas utilizadas para monitorar, supervisionar e, em alguns casos, controlar processos industriais em tempo real.

Eles são amplamente utilizados em setores como:
- Indústria de manufatura  
- Energia elétrica  
- Saneamento  
- Petróleo e gás  
- Automação predial  

O SCADA não substitui o CLP. Cada um tem um papel específico:

- **CLP (Controlador Lógico Programável):**
  - Responsável pelo controle direto do processo  
  - Executa lógica em tempo real  
  - Atua diretamente sobre sensores e atuadores  

- **SCADA:**
  - Responsável pela supervisão  
  - Exibe dados para operadores  
  - Registra históricos  
  - Permite análise e tomada de decisão  

---

### 📊 Arquitetura de um sistema SCADA

A arquitetura é geralmente dividida em três níveis:

#### 1. Nível de Campo
- Sensores (temperatura, pressão, nível)  
- Atuadores (válvulas, motores)  
- Dispositivos físicos  

#### 2. Nível de Controle
- CLPs  
- Controladores industriais  
- Sistemas embarcados  

#### 3. Nível de Supervisão
- Software SCADA  
- Interface gráfica (IHM)  
- Servidores e estações de operação  

Fluxo típico:

Sensor → CLP → SCADA → Operador

---

### 🖥️ IHM (Interface Homem-Máquina)

A IHM é a interface visual do sistema. É através dela que o operador:

- Visualiza dados  
- Interage com o sistema  
- Envia comandos  
- Monitora alarmes  

---

### 🌐 Tipos de sistemas SCADA

#### Centralizado
- Um único servidor controla tudo  
- Mais simples  
- Menor escalabilidade  

#### Distribuído
- Vários servidores e clientes  
- Alta escalabilidade  
- Maior robustez  
- Mais usado na indústria moderna  

---

### ⚙️ Funcionamento básico

1. Sensores captam dados do processo  
2. CLP processa os dados  
3. SCADA coleta esses dados via comunicação  
4. Dados são exibidos na interface  
5. Operador toma decisões  

---

### 🧩 Integração com CLP

A integração é feita por meio de protocolos de comunicação.

O SCADA lê e escreve dados no CLP através de:
- Tags  
- Endereços de memória  
- Variáveis de processo  

---

## 🔧 Ferramentas relacionadas  

### 🛠️ Elipse E3
- Muito usado no Brasil  
- Forte em integração industrial  

### 🛠️ Siemens WinCC
- Integrado com sistemas Siemens  
- Muito usado em grandes indústrias  

### 🛠️ Ignition SCADA
- Plataforma moderna  
- Baseada em web  
- Usa Python para scripts  

---

## 💻 Exemplo prático  

### 🎯 Cenário: Controle de nível de tanque

Fluxo:

Sensor de nível → CLP → SCADA → Operador

Passo a passo:

1. Sensor mede nível do tanque  
2. CLP recebe sinal (ex: 4-20mA)  
3. CLP converte em valor digital  
4. SCADA lê o valor  
5. SCADA exibe na tela  

Exemplo simplificado:


Nível = 75%
Status = OK
Bomba = Ligada


---

## ⚠️ Erros comuns  

- Confundir SCADA com CLP  
- Achar que SCADA controla diretamente o processo  
- Ignorar a importância da comunicação  
- Não entender a arquitetura em níveis  
- Achar que IHM e SCADA são sempre a mesma coisa  
- Não considerar escalabilidade  
- Subestimar a importância da supervisão  

---

## 📝 Resumo  

- SCADA = supervisão e aquisição de dados  
- CLP = controle do processo  
- IHM = interface visual  
- Arquitetura:
  - Campo  
  - Controle  
  - Supervisão  
- Fluxo:
  Sensor → CLP → SCADA → Operador  
- Pode ser:
  - Centralizado  
  - Distribuído  

---

## 📖 Referências  

- BOYER, Stuart A. *SCADA: Supervisory Control and Data Acquisition*. ISA, 2009.  
- RODRÍGUEZ PENÍN, Aquilino. *Sistemas SCADA: guía práctica*. Marcombo, 2007.  
- GARCIA JUNIOR, Ervaldo. *Introdução a sistemas de supervisão, controle e aquisição de dados*. 2019.  
