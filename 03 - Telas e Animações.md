# Telas e Animação em SCADA (IHM)

## 🎯 Objetivo  
Criar interfaces gráficas para interação com o sistema, permitindo ao operador visualizar, monitorar e controlar processos industriais de forma intuitiva.

---

## 📚 Conceitos-chave  
- Telas (screens)  
- Objetos gráficos  
- Objetos de animação  
  - Cor  
  - Movimento  
  - Visibilidade  
- Navegação entre telas  
- Interface Homem-Máquina (IHM)  
- Usabilidade  
- Design industrial  
- Feedback visual  
- Interação com operador  

---

## 🧠 Explicação  

A IHM (Interface Homem-Máquina) é a camada visual do sistema SCADA. É por meio dela que o operador acompanha o processo industrial e toma decisões.

Uma boa interface deve ser:
- Clara  
- Intuitiva  
- Rápida  
- Segura  

---

### 🖥️ Telas (Screens)

As telas representam diferentes partes do sistema.

Exemplos:
- Tela geral da planta  
- Tela de tanque  
- Tela de alarmes  
- Tela de manutenção  

Cada tela contém objetos que representam o processo.

---

### 🔲 Objetos gráficos

São os elementos visuais usados na interface.

Exemplos:
- Botões  
- Indicadores  
- Barras de nível  
- Tanques  
- Motores  
- Válvulas  

Esses objetos podem ser:
- Estáticos (apenas visual)  
- Dinâmicos (interagem com dados)  

---

### 🎞️ Objetos de animação

Permitem representar o comportamento do processo em tempo real.

#### 🎨 Cor
- Verde = ligado  
- Vermelho = desligado  
- Amarelo = alerta  

#### 🔄 Movimento
- Rotação de motor  
- Fluxo de líquido  
- Movimento de válvula  

#### 👁️ Visibilidade
- Mostrar/esconder elementos  
- Exibir alarmes  
- Indicar estados  

---

### 🔗 Navegação

Permite alternar entre telas.

Pode ser feita por:
- Botões  
- Menus  
- Links  

Exemplo:
- Tela principal → Tela de tanque → Tela de manutenção  

---

### ⚙️ Boas práticas de interface

- Evitar excesso de informação  
- Usar cores padronizadas  
- Manter consistência visual  
- Facilitar leitura rápida  
- Destacar alarmes  

---

## 🔧 Ferramentas relacionadas  

### 🛠️ Editor gráfico SCADA
- Ambiente para criação de telas  
- Permite inserir objetos e animações  

### 🛠️ Bibliotecas industriais
- Conjunto de símbolos prontos  
- Motores, válvulas, tanques  
- Acelera desenvolvimento  

---

## 💻 Exemplo prático  

### 🎯 Cenário: Tela de tanque

Componentes:

- Tanque com nível  
- Botão liga/desliga bomba  
- Indicador de status  

---

### 🧩 Estrutura da tela


[ TANQUE ]
| |
| 70% |
| |

Botão: Ligar bomba
Status: Ligado


---

### 🔗 Ligação com tags


Tag: Nivel_Tanque → animação de altura
Tag: Bomba → cor do botão
Tag: Status → texto na tela


---

### 🔄 Exemplo de animação

- Se `Bomba = TRUE` → botão verde  
- Se `Bomba = FALSE` → botão vermelho  

---

### 🖱️ Interação

- Clique no botão → envia comando ao CLP  
- SCADA atualiza estado  
- Interface reflete mudança  

---

## ⚠️ Erros comuns  

- Interface poluída  
- Uso excessivo de cores  
- Falta de padrão visual  
- Objetos sem ligação com tags  
- Animações confusas  
- Falta de feedback ao usuário  
- Navegação complicada  
- Informação irrelevante na tela  

---

## 📝 Resumo  

- IHM é a interface do operador  
- Telas organizam o sistema  
- Objetos representam o processo  
- Animações mostram comportamento  
- Navegação conecta telas  
- Interface deve ser simples e clara  

---

## 📖 Referências  

- BOYER, Stuart A. *SCADA: Supervisory Control and Data Acquisition*. ISA, 2009.  
- RODRÍGUEZ PENÍN, Aquilino. *Sistemas SCADA: guía práctica*. Marcombo, 2007.  
- GARCIA JUNIOR, Ervaldo. *Introdução a sistemas de supervisão, controle e aquisição de dados*. 2019.  
- JENNINGS, Richard; CUEVA, Fabiola. *LabVIEW graphical programming*. 2019.  
