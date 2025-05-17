# 🧱 Processamento e Engenharia de Dados

Antes de aplicar algoritmos de Machine Learning, é essencial garantir que os dados estejam limpos, organizados e no formato adequado. Esse processo é conhecido como **Pré-processamento de Dados** e **Engenharia de Atributos** (ou *Feature Engineering*).

---

## 1. 🧹 Limpeza de Dados (*Data Cleaning*)

A qualidade dos dados influencia diretamente a qualidade dos modelos. Dados sujos geram modelos ruins.

### Principais etapas da limpeza:

- **Valores ausentes (nulos):**
  - Remover, preencher com média/mediana/moda, ou aplicar técnicas mais avançadas.
- **Duplicatas:**  
  - Linhas idênticas que devem ser removidas.
- **Erros e inconsistências:**  
  - Corrigir nomes, formatos e padrões (como datas escritas de forma diferente).
- **Outliers (valores muito fora do padrão):**
  - Identificar com gráficos ou estatísticas e decidir se devem ser tratados ou removidos.

### 🧪 Exemplo prático com Pandas:

```python
import pandas as pd

# Carregando os dados
df = pd.read_csv("dados.csv")

# Verificando valores nulos
print(df.isnull().sum())

# Preenchendo valores nulos com a média da coluna "idade"
df['idade'] = df['idade'].fillna(df['idade'].mean())

# Removendo linhas duplicadas
df = df.drop_duplicates()

# Padronizando textos: tudo em minúsculas na coluna "nome"
df['nome'] = df['nome'].str.lower()
```

---

## 2. 🔄 Transformação de Dados
Transformações tornam os dados mais adequados para os modelos. Algumas técnicas comuns:

## 🟦 Normalização
Transforma os valores para uma escala de 0 a 1. Útil para distâncias, KNN, etc.

```python
from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler()
df[['altura', 'peso']] = scaler.fit_transform(df[['altura', 'peso']])
```

## 🟨 Padronização
Transforma os dados para média 0 e desvio padrão 1. Recomendado para algoritmos que assumem distribuição normal (ex: Regressão Linear, SVM).

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
df[['altura', 'peso']] = scaler.fit_transform(df[['altura', 'peso']])
```

## 🟪 One-Hot Encoding
Converte variáveis categóricas em colunas binárias.
```python
# Converte a coluna 'sexo' para colunas binárias
df = pd.get_dummies(df, columns=['sexo'])
```

## 🟧 Transformações logarítmicas
Reduz a assimetria de colunas com valores muito altos ou dispersos.

```python
import numpy as np

df['renda_log'] = np.log(df['renda'] + 1)  # Evita log(0)
```
---

## 3. 🔧 Engenharia de Atributos (Feature Engineering)
Criar novas variáveis (features) a partir das existentes pode melhorar o desempenho dos modelos.

### Exemplos práticos:
* Agrupamentos ou faixas de valores:
```python
# Criando faixas de idade
df['faixa_idade'] = pd.cut(df['idade'], bins=[0, 18, 35, 60, 100], labels=["jovem", "adulto", "meia-idade", "idoso"])
```

* Combinação de variáveis:
```python
# Criando uma nova coluna combinando cidade e estado
df['local'] = df['cidade'] + "-" + df['estado']
```

* Extração de dados de colunas tipo data:
```python
# Convertendo para datetime e extraindo informações
df['data'] = pd.to_datetime(df['data'])
df['ano'] = df['data'].dt.year
df['mes'] = df['data'].dt.month
df['dia_semana'] = df['data'].dt.day_name()
```
---

## ✅ Resumo



| Etapa               | O que faz?
|---------------------|----------------------------------------------------------|
| **Limpeza de Dados**   | Remove ou corrige dados inválidos              |
| **Transformação**     | Ajusta os valores para melhorar a performance dos modelos      |
| **MEngenharia de Atributos** | Cria novas variáveis mais representativas |

