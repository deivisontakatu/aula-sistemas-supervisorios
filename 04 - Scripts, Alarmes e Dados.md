# Scripts, Alarmes e Dados em SCADA

## 🎯 Objetivo  
Adicionar lógica, monitoramento e registro de dados ao sistema SCADA, permitindo automação inteligente e análise do processo industrial.

---

## 📚 Conceitos-chave  
- Scripts  
- Automação lógica  
- Eventos  
- Alarmes  
  - Tipos de alarmes  
  - Prioridade  
  - Reconhecimento  
- Históricos  
- Tendências (gráficos)  
- Relatórios  
- Banco de dados (SQL)  
- Registro de eventos  
- Análise de dados  

---

## 🧠 Explicação  

Além de visualizar dados, o SCADA também pode tomar decisões e registrar informações.  
Isso é feito por meio de scripts, alarmes e armazenamento de dados.

---

### ⚙️ Scripts

Scripts são códigos executados dentro do SCADA para automatizar ações.

Podem ser usados para:
- Tomar decisões  
- Executar comandos  
- Manipular dados  
- Criar lógica personalizada  

Linguagens comuns:
- VBScript  
- Python  

---

### 🔔 Alarmes

Alarmes são eventos que indicam condições anormais no processo.

#### Tipos de alarmes:
- Alto (High)  
- Baixo (Low)  
- Crítico  
- Falha  

#### Prioridade:
- Alta  
- Média  
- Baixa  

#### Reconhecimento:
- O operador confirma o alarme  
- O sistema registra a ação  

---

### 🗄️ Históricos

Históricos armazenam dados ao longo do tempo.

Permitem:
- Análise de desempenho  
- Identificação de falhas  
- Auditoria  

Exemplo:
- Temperatura registrada a cada minuto  

---

### 📈 Tendências (gráficos)

Mostram a evolução dos dados ao longo do tempo.

Exemplo:
- Gráfico de temperatura  
- Gráfico de nível  

---

### 📄 Relatórios

Geram documentos com dados do processo.

Podem conter:
- Valores médios  
- Eventos  
- Alarmes  
- Produção  

---

### 🧮 Banco de dados (SQL)

Os dados do SCADA são armazenados em bancos de dados.

Funções:
- Armazenar históricos  
- Gerar relatórios  
- Consultar dados  

Exemplo de banco:
- MySQL  
- SQL Server  

---

### 🔄 Fluxo de dados


Sensor → CLP → SCADA → Banco de Dados → Relatório


---

## 🔧 Ferramentas relacionadas  

### 🛠️ Scripts
- VBScript  
- Python  

### 🛠️ SQL
- MySQL  
- SQL Server  

### 🛠️ Trend charts
- Gráficos de tendência  
- Visualização de dados  

---

## 💻 Exemplo prático  

### 🎯 Criando um alarme

Condição:
- Se nível > 90% → alarme alto  

Pseudo código:


IF Nivel_Tanque > 90 THEN
Alarme = TRUE
END IF


---

### 📈 Gerando histórico

Exemplo de registro:


Hora | Nivel
10:00 | 70%
10:01 | 72%
10:02 | 75%


---

### 📊 Gráfico de tendência

- Eixo X: tempo  
- Eixo Y: valor  

---

### 🧾 Consulta SQL simples


SELECT * FROM historico_nivel
WHERE Nivel > 80


---

## ⚠️ Erros comuns  

- Não configurar alarmes corretamente  
- Ignorar prioridade de alarmes  
- Criar scripts complexos demais  
- Não testar lógica  
- Não armazenar dados corretamente  
- Banco de dados mal estruturado  
- Não registrar histórico suficiente  
- Falta de backup  
- Gráficos sem sentido  
- Relatórios confusos  

---

## 📝 Resumo  

- Scripts adicionam lógica  
- Alarmes indicam falhas  
- Históricos registram dados  
- Tendências mostram evolução  
- Relatórios organizam informações  
- SQL armazena dados  

---

## 📖 Referências  

- BOYER, Stuart A. *SCADA: Supervisory Control and Data Acquisition*. ISA, 2009.  
- RODRÍGUEZ PENÍN, Aquilino. *Sistemas SCADA: guía práctica*. Marcombo, 2007.  
- GARCIA JUNIOR, Ervaldo. *Introdução a sistemas de supervisão, controle e aquisição de dados*. 2019.  
- PETRUZZELLA, F. D. *Controladores Lógicos Programáveis*. 2014.  

---

## 🚀 Desafio / Exercício  

### 🧠 Exercício 1
Crie um alarme para:
- Temperatura alta (> 80°C)  

---

### 🧠 Exercício 2
Defina:
- Tipo de alarme  
- Prioridade  
- Ação  

---

### 🧠 Exercício 3
Crie um script simples para:
- Ligar uma bomba automaticamente  

---

### 🧠 Exercício 4
Explique o fluxo:


Sensor → CLP → SCADA → Banco


---

### 🧠 Exercício 5
Descreva como funciona um gráfico de tendência.

---

### 🧠 Exercício 6
Crie uma tabela SQL para armazenar nível.

---

### 🧠 Exercício 7
Explique a diferença entre:
- Histórico  
- Tendência  

---

### 🧠 Exercício 8
Liste 3 tipos de alarmes.

---

### 🧠 Exercício 9
Explique o papel do banco de dados no SCADA.

---

### 🧠 Exercício 10
Descreva como gerar um relatório.

---

## 🧩 Expansão do conteúdo  

- Big Data industrial  
- IoT  
- Machine Learning em SCADA  
- Analytics  
- Data Lake  

---

## 📌 Observação final  

A inteligência do SCADA está nos dados e na lógica.  
Sem isso, ele é apenas um sistema de visualização.  

Scripts, alarmes e históricos transformam dados em informação útil.

---