# 🚕 Análise de Dados de Táxi - Chicago

## 🎯 Sobre o Projeto
Projeto de análise de dados combinando SQL e Python para investigar padrões de uso de táxi em Chicago. O projeto explora dados de corridas, comportamento por empresa, destinos populares e testa hipóteses sobre fatores que influenciam a duração das viagens.

## 🔍 Contexto do Negócio
Empresas de táxi precisam entender:
- Quais regiões têm maior demanda
- Como diferentes empresas competem no mercado
- Fatores externos (como clima) que afetam as operações
- Otimização de rotas e tempos de viagem

## 📂 Dados Utilizados

### **Dataset 1: Corridas por Empresa**
`project_sql_result_01.csv`
- **trips_amount:** número de corridas por empresa de táxi
- **Período:** 15-16 de novembro de 2017

### **Dataset 2: Destinos por Bairro**
`project_sql_result_04.csv`
- **dropoff_location_name:** bairros de Chicago onde corridas terminaram
- **average_trips:** média de viagens finalizadas por bairro
- **Período:** novembro de 2017

### **Dataset 3: Teste de Hipótese**
`project_sql_result_07.csv`
- **Rota específica:** Loop → Aeroporto Internacional O'Hare
- **start_ts:** data/hora de início da corrida
- **weather_conditions:** condições climáticas
- **duration_seconds:** duração da corrida em segundos

## 🛠️ Metodologia

### **Fase 1: Extração de Dados (SQL)**
- Consultas SQL para agregação e filtragem de dados
- Integração de múltiplas tabelas
- Análise temporal e geográfica

### **Fase 2: Análise Exploratória (Python)**
- Importação e validação de dados
- Verificação de tipos de dados
- Identificação de padrões e outliers
- Análise dos top 10 bairros mais populares

### **Fase 3: Visualização**
- Gráfico: Empresas de táxi vs. número de corridas
- Gráfico: Top 10 bairros por destino
- Análise comparativa entre empresas
- Distribuição geográfica da demanda

### **Fase 4: Teste de Hipótese Estatística**
**Hipótese testada:**
> "A duração média das viagens do Loop para o Aeroporto O'Hare muda nos sábados chuvosos"

**Abordagem estatística:**
- **Hipótese Nula (H₀):** A duração média é igual em sábados chuvosos e não-chuvosos
- **Hipótese Alternativa (H₁):** A duração média é diferente em sábados chuvosos
- **Teste utilizado:** Teste t de Student (ou Mann-Whitney U, se não-paramétrico)
- **Nível de significância (α):** 0.05
- **Critério de decisão:** p-value < α rejeita H₀

## 💻 Tecnologias Utilizadas
- **SQL** - extração e agregação de dados
- **Python 3.x**
- **pandas** - manipulação de dados
- **numpy** - operações numéricas
- **matplotlib / seaborn** - visualização
- **scipy.stats** - testes estatísticos
- **Jupyter Notebook** - desenvolvimento

## 📈 Principais Resultados

### **Análise de Empresas**
[Descreva aqui os principais achados sobre distribuição de corridas entre empresas]

### **Top 10 Bairros**
[Liste os 10 bairros mais populares e insights sobre eles]

### **Teste de Hipótese**
**Resultado do teste:**
- p-value: [seu resultado]
- Conclusão: [rejeita ou não rejeita H₀]
- Interpretação: [explicação do que isso significa na prática]

### **Insights de Negócio**
✓ [Insight 1 sobre padrões de demanda]
✓ [Insight 2 sobre impacto do clima]
✓ [Insight 3 sobre competição entre empresas]
✓ [Recomendações operacionais]

## 📊 Visualizações
O projeto inclui visualizações para:
- Distribuição de corridas por empresa
- Ranking de bairros mais populares como destino
- Comparação de durações de viagem por condição climática
- Análise temporal de padrões de uso

## 🚀 Como Executar

### Pré-requisitos
```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

### Estrutura de arquivos
```
├── README.md
├── sprint_7_analise_taxi_chicago.ipynb
└── dados/
    ├── project_sql_result_01.csv
    ├── project_sql_result_04.csv
    └── project_sql_result_07.csv
```

### Executando
1. Clone este repositório
2. Coloque os arquivos CSV na pasta `dados/`
3. Abra o Jupyter Notebook:
```bash
jupyter notebook sprint_7_analise_taxi_chicago.ipynb
```

## 💡 Competências Demonstradas
Este projeto demonstra:
- **SQL:** extração e agregação de dados relacionais
- **Python:** análise e manipulação de dados
- **Estatística:** formulação e teste de hipóteses
- **Visualização:** comunicação clara de insights
- **Pensamento crítico:** interpretação de resultados
- **Análise de negócios:** recomendações práticas

## 🎓 Contexto Acadêmico
**Sprint 7 - Bootcamp de Ciência de Dados TripleTen (2024)**

Este projeto integra SQL e Python para análise completa de dados do mundo real, demonstrando pipeline end-to-end de análise de dados.

---

**Desenvolvido por:** Diogo  
**GitHub:** [@zDiogoTM](https://github.com/zDiogoTM)
