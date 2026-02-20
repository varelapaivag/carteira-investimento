
---

## 📥 Coleta e Tratamento dos Dados

- Dados financeiros obtidos via APIs públicas
- Padronização das séries temporais em base diária
- Ajuste de frequência do IPCA (mensal → diária via forward fill)
- Consolidação das bases por data
- Normalização dos dados com **MinMaxScaler**

---

## 📈 Retornos Utilizados

O projeto utiliza **retorno logarítmico** como métrica principal, pois:

- É **aditivo no tempo**
- Elimina distorções do retorno simples
- Representa melhor o efeito acumulado das variações
- É mais adequado para análise de portfólios

---

## 📊 Análises Realizadas

### 🔹 Análise Exploratória
- Visualização conjunta de ativos vs indicadores macro
- Comparação de comportamento relativo ao mercado

### 🔹 Análise Temporal
- Variação média mensal
- Variação média anual
- Volatilidade (desvio padrão)

### 🔹 Regressão com Benchmark
- Estimação de **Beta**
- Avaliação de **R²**
- Relação risco sistêmico × retorno

### 🔹 Dividendos
- Consolidação mensal de dividendos
- Análise do total distribuído por ativo
- Integração com retorno total

---

## 🎲 Simulação de Monte Carlo

- Simulação de múltiplos cenários de evolução da carteira
- Avaliação da distribuição dos montantes finais
- Análise de risco via:
  - Distribuição
  - Boxplot
  - Estatísticas descritivas

---

## ⚙️ Otimização da Carteira

### Update — Otimização do modelo anterior

A otimização proposta corrige limitações importantes do modelo clássico de Markowitz.

📌 **Principais melhorias técnicas**:

- A penalização **não depende do número de ativos**
- A penalização atua sobre **concentração informacional**, e não de forma arbitrária
- Maior estabilidade dos pesos
- Melhor interpretação econômica do portfólio resultante

Os pesos são normalizados garantindo que a soma seja igual a 1.
