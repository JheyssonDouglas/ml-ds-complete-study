# 📗 Matemática e Estatística para Ciência de Dados

## 📌 Por que matemática e estatística são importantes?

Ciência de Dados não é só programação e ferramentas. A base para entender os dados, construir modelos, interpretar resultados e tomar decisões está na matemática e estatística.

Imagine matemática e estatística como a **linguagem** que os dados falam. Sem essa linguagem, não conseguimos interpretar corretamente o que os dados querem dizer.

---

## 1. Conceitos Básicos de Matemática

### 1.1 Números e Operações Fundamentais

- **Números reais**: qualquer número que pode ser representado em uma reta, incluindo inteiros, frações e decimais.
- **Operações básicas**: adição (+), subtração (−), multiplicação (×) e divisão (÷).
- **Potenciação e radiciação**: elevar um número a uma potência (ex: $2^3 = 8$) e a raiz (ex: $\sqrt{9} = 3$).

---

### 1.2 Álgebra Linear

Fundamental para manipular dados em múltiplas dimensões.

- **Vetores**: lista ordenada de números. Ex: $\mathbf{v} = [2, 3, 5]$
- **Matrizes**: tabelas de números organizados em linhas e colunas.

Exemplo:  
$
A = \begin{bmatrix}
1 & 2 \\
3 & 4 \\
\end{bmatrix}
$

- **Operações com matrizes**: soma, multiplicação, transposição.
- **Produto escalar**: multiplicação de vetores que resulta em um número, usado para medir similaridade.

---

### 1.3 Cálculo Diferencial e Integral (Noções básicas)

- **Derivada**: mede a taxa de variação de uma função — quão rápido algo muda.
- **Integral**: soma acumulada, área sob a curva.

Esses conceitos ajudam, por exemplo, a entender como os modelos aprendem (otimização).

---

## 2. Estatística

### 2.1 Estatística Descritiva

Resumo dos dados para entender sua distribuição e características.

- **Média ($\bar{x}$)**: valor médio dos dados.
- **Mediana**: valor central quando os dados estão ordenados.
- **Moda**: valor que aparece com maior frequência.
- **Variância ($\sigma^2$)**: mede a dispersão dos dados em relação à média.
- **Desvio padrão ($\sigma$)**: raiz quadrada da variância, indica quanto os dados se afastam da média.

Exemplo:  
Dados: 2, 4, 4, 6, 8  
- Média = $\frac{2 + 4 + 4 + 6 + 8}{5} = 4.8$
- Mediana = 4 (valor central)  
- Moda = 4 (mais frequente)  
- Variância = $\frac{(2 - 4.8)^2 + (4 - 4.8)^2 + (4 - 4.8)^2 + (6 - 4.8)^2 + (8 - 4.8)^2}{5} = 4.56$   
- Desvio padrão = $\sqrt{4.56} \approx 2.14$

---

### 2.2 Probabilidade

Probabilidade é a medida da chance de um evento ocorrer.

- Vai de 0 (impossível) a 1 (certeza).
- Eventos podem ser independentes, mutuamente exclusivos, etc.

Exemplo:  
A probabilidade de tirar um número 4 em um dado comum de 6 lados é $ \frac{1}{6} \approx 0.1667 $.

---

### 2.3 Distribuições de Probabilidade

Funções que descrevem como os dados se comportam.

- **Distribuição Uniforme**: todos os valores têm a mesma probabilidade.
- **Distribuição Normal (Gaussiana)**: curva em forma de sino, muito comum na natureza e dados reais.
- **Distribuição Binomial**: sucesso/falha em vários testes (ex: número de caras ao jogar moeda).

---

### 2.4 Testes Estatísticos

Para validar hipóteses e tirar conclusões.

- **Hipótese nula ($H_0$)**: afirmação padrão que queremos testar.
- **Teste t, qui-quadrado, ANOVA**: diferentes testes para comparar médias, frequências etc.
- **p-valor**: probabilidade de obter um resultado igual ou mais extremo que o observado, assumindo que $H_0$ é verdadeira. Se for menor que um nível (ex: 0.05), rejeitamos $H_0$.

---

### 2.5 Correlação e Covariância

Medem a relação entre duas variáveis.

- **Covariância**: indica a direção da relação (positiva ou negativa).
- **Correlação**: mede força e direção da relação, varia de -1 (inversamente correlacionadas) a +1 (fortemente correlacionadas).

---

## 3. Aplicações Práticas

### 3.1 Por que aprender isso tudo?

- Para interpretar corretamente os dados e os resultados dos modelos.
- Para escolher o modelo certo para o problema.
- Para avaliar se os resultados são confiáveis.
- Para explicar os resultados a pessoas não técnicas.

### 3.2 Dicas para aprender matemática e estatística

- Pratique com exemplos reais.
- Use ferramentas visuais (gráficos, plots).
- Faça pequenos projetos aplicando conceitos.
- Use cursos e livros indicados (vou sugerir no final).

---

## 4. Recursos Recomendados

- Livro: *Estatística Básica* – Wilton O. Bussab e Pedro A. Morettin
- Livro: *Matemática para Machine Learning* – Marc Peter Deisenroth, A. Aldo Faisal, Cheng Soon Ong
- Curso: *Probabilidade e Estatística* (Khan Academy)
- Curso: *Matemática para Data Science* (Coursera)
- Ferramenta: [Khan Academy](https://pt.khanacademy.org/math/statistics-probability)

---

## 📌 Resumo

| Tema                     | O que é / para que serve                          |
|--------------------------|--------------------------------------------------|
| Álgebra Linear           | Manipular dados multidimensionais                 |
| Cálculo                  | Entender mudanças e otimizar modelos              |
| Estatística Descritiva   | Resumir e entender dados                           |
| Probabilidade            | Medir chances e incertezas                          |
| Distribuições            | Modelar o comportamento dos dados                  |
| Testes Estatísticos      | Validar hipóteses e conclusões                      |
| Correlação e Covariância | Medir relações entre variáveis                      |

---