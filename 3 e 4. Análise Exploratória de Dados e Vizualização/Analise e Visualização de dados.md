<h1>Análise e Visualização de dados </h1>
<h2> Análise exploratória de dados </h2>

É a análise de conjunto de dados e resumo de suas principais características. 

Ela pode ajudar na identificação de erros e entender melhor os padrões presentes dos dados, detectar desvios ou eventos anômalos, além de encontrar relações interessantes entre as variáveis.

Tipos de análises:

- **Univariada sem gráficos.** Os dados que estão sendo analisados consistem em apenas uma variável. Como é uma única variável, ela não lida com causas ou relacionamentos. O principal objetivo da análise univariada é descrever os dados e encontrar padrões que existem dentro dela.
- **Univariada com gráficos.** Os métodos não gráficos não fornecem uma imagem completa dos dados. Os métodos gráficos são, portanto, necessários. Tipos comuns de gráficos univariados incluem:
    - As tabelas cruzadas, que mostram todos os valores de dados e a forma da distribuição.
    - Histogramas, que são gráficos de colunas em que cada coluna representa a frequência (contagem) ou proporção (contagem/contagem total) de casos para um intervalo de valores.
    - Diagramas de caixa, que retratam graficamente o resumo dos cinco números, do mínimo, primeiro quartil, mediana, terceiro quartil e máximo.
- **Multivariada sem gráficos:** Dados multivariados são extraídos de mais de uma variável. As técnicas de EDA multivariadas sem gráficos geralmente mostram a relação entre duas ou mais variáveis dos dados por meio de tabulação cruzada ou estatística.
- **Multivariada com gráficos:** Dados multivariados usam gráficos para exibir relações entre dois ou mais conjuntos de dados. O gráfico mais utilizado é o gráfico de colunas agrupadas ou diagrama de colunas com cada grupo representando um nível de uma das variáveis e cada coluna dentro de um grupo que representa os níveis da outra variável.

O **Python** e o **R** são as linguagens mais utilizadas para análise de dados.

As bibliotecas de Python mais utilizadas são o **Pandas**, **Seaborn** e **Matplotlib**. 

Para se trabalhar com Pandas e o Seaborn, é necessário estar familiarizado com
duas estruturas de dados que são: **Séries** e **Dataframes.**

**Séries**

É um array unidimensional, semelhante a uma lista em Python, no entanto criado sobre o numpy.

Várias series juntas (nseries) formam um dataframe.

**Dataframe**

O dataframe é um tipo de matriz com diversos tipos de dados.

É uma estrutura de dados tabular bidimensional e mutável em tamanho, potencialmente heterogênea, com eixos rotulados (linhas e colunas). Para se criar um Dataframe a partir das estruturas de dados nativas em Python, pode-se passar um dicionário de listas para seu construtor.

[Data sheets](https://www.datacamp.com/cheat-sheet)

Comandos mais comuns em um Dataframe

**df.shape() -** Quantidade de linhas e colunas do Dataframe
**df.head() -** Primeiros 5 registros do Dataframe
**df.tail()** **-** Últimos 5 registros do Dataframe
**df.columns() -** Colunas presentes no Dataframe
**df.count () -** Contagem de dados não-nulos
**df.sum() -** Soma dos valores de um Dataframe
**df.min() -** Menor valor de um Dataframe
**df.max() -** Maior valor de um Dataframe
**df.describe() -** Resumo estatístico do Dataframe

### **Compreendendo dados**

**Contínuos x Categóricos**

- **Contínuos**: Faixa de dados contínua. Quantitativo. Exemplo: margem de lucro, altura da montanha.
- **Categóricos**: Não contínuo. Qualitativo: Exemplo: Modelo de carro, tipo de produto.
- **Discreto**: Pode ser quantitativo ou qualitativo. Tem valores inteiros não negativos. Exemplo: número de maçãs em um barril.

**Quantitativo x Qualitativo**

**Qualitativo** 

- **Nominal**: dados em que você pode distinguir valores diferentes, mas não necessariamente ordena-los
- **Ordinal**: dados ordenados em uma classificação existente (pequeno, médio, grande)

**Quantitativo**

- **Intervalo**: Dados como dados ordinais, mas a distância entre os pontos de dados é uniforme. Nem todas as operações aritméticas podem ser executadas.
- **Proporção**: Dados compostos de os outros atributos e todas as operações aritméticas podem ser executadas.

### Medidas de tendência central ou de posição

- **Media:** Soma dos valores observados dividida pelo número desses valores.

É calculado no python através do **.mean()**

- **Mediana:** É o valor médio ou a média aritmética de dois valores centrais de um conjunto
de números ordenados (crescente ou decrescente). Para calculá-la, primeiramente temos
de reorganizar os dados em ordem crescente (ou decrescente) e, em seguida, escolher o
valor central. É calculado no python através do **.median()**
- **Moda**: Valor que ocorre com maior frequência em um dado conjunto de dados. Se todos os valores aparecem um número igual de vezes (em geral, uma vez cada), dizemos que o conunto de dados não têm moda. É calculado no python através do **.mode()**

### Medidas de dispersão ou variablidade

- **Amplitude**: É a diferença entre o maior valor e o menor valor.  **.max() - .min()**
- **Variância**: É a média dos quadrados dos desvios das medidas em relação à sua média x. É calculado no python através do **.var()**

- **Desvio padrão**: A raiz quadrada da média aritmética dos quadrados dos
desvios em relação à média. É calculado no python através do **.std()**

O pandas disponibiliza a função **describe()** que gera as estatísticas descritivas.

### Quartis, decis, percentis e “N”is

A mediana divide as amostras em dois conjuntos de dados.

Mas podemos dividir nossos dados em **N** partes. Os valores que dividem os dados em N partes se chamam **separatrizes**.

Vamos estudar a principal utilizada na estatística descritiva: os quartis.

Se você entender a ideia do quartis, basta apenas aplicar os conceitos e fórmulas para decis, percentis ou qualquer quantidade de separatrizes que deseje utilizar em seus dados.

Os quartis dividem nosso conjunto de dados em quatro partes iguais. Para isso precisamos de três pontos de cortes.


### Visualização gráfica de dados

- **Histograma**: Representa a distribuição dos dados, formando compartimentos ao longo do
intervalo dos dados. O seaborn disponibiliza a função **distplot()** para “plotar” histogramas. Essa função combina a função **hist** do matplotlib com as funções **kdeplot()** e **rugplot()** do próprio seaborn.

- **Gráfico de barra e linhas**: No gráﬁco de barras, cada categoria é representada por uma barra de comprimento proporcional à sua frequência, conforme identiﬁcação no eixo horizontal. O
seaborn disponibiliza a função **catplot()** para “plotar” gráﬁcos de barra. Para “plotar” gráﬁcos de linha, o seaborn disponibiliza a função **relplot ().**

- **Gráfico de setores:** Este gráﬁco é constituído com base em um círculo, e é empregado sempre que desejamos ressaltar a participação do dado em relação ao total.
Existem algumas recomendações devem ser seguidas ao se elaborar gráﬁcos de setores. Os valores devem ser apresentados em ordem decrescente a partir da parte superior do gráﬁco e no sentido horário. Ao lado de cada setor, podem-se colocar os percentuais e os nomes de cada parcela. Não é recomendado a utilização deste gráﬁco usado quando há muitas parcelas e nem quando existem muitas parcelas com valores muito semelhantes, sob pena de se perder uma das suas principais funções: a da comparação. Para “plotar” gráﬁcos de setores é necessário a utilização da função **matplotlib.pyplot.pie** do mat plotlib.


- **Boxplots**: É um gráﬁco apresentado em formato de caixa, em que a aresta inferior da caixa representa o primeiro quartil (Q1), a aresta superior representa o terceiro quartil (Q3) e um traço interno à caixa representa a mediana (Q2) de uma amostra. Para “plotar” boxplot, o seaborn disponibiliza a função **boxplot().**

- **Gráfico de dispersão**: São utilizados para pontuar dados em um eixo vertical e horizontal
com a intenção de exibir quanto uma variável é afetada por outra. O seaborn disponibiliza a função **catplot().**

### Valores Faltantes

**Os *outliers* são dados que se diferenciam drasticamente de todos os outros.**

Entender os outliers é fundamental em uma análise de dados por pelo menos dois aspectos:

1. os outliers podem viesar negativamente todo o resultado de uma análise;
2. o comportamento dos *outliers* pode ser justamente o que está sendo procurado.

Os outliers presentes em datasets possuem diversos outros nomes, como:

1. dados discrepantes;
2. pontos fora da curva; 
3. observações fora do comum;
4. anomalias;
5. valores atípicos;
6. entre outros.

O que podemos fazer com valores faltantes(missing values/outliers)?

- **Excluir os valores**: Terá um modelo mais robusto, **mas** pode haver perda de informação e o modelo pode ficar ruim se houver muitos valores faltantes;
- **Substitua pela média/mediana**: Não haverá perda de dados e funciona bem com um dataset pequeno, **mas** só funciona com valores numéricos e contíno e não leva em consideração a covariância dos fatores;
- **Substitua pela moda ou criar uma nova categoria**: Não haverá perda de dados e funciona bem com um dataset pequeno, **mas** só funciona com valores categóricos e pode levar a baixa performance;
- **Criar um modelo para isso**: pode dar ótimos resultados e leva em consideração a covariância dos dados, mas é muito mais trabalhoso e é um proxy para os valores verdadeiros.

<h2> Visualização de Dados </h2>
É a representação e apresentação gráfica dos dados.

Objetivo>

- Criar visualizações com dados brutos para contas histórias;
- Entender e gerar conclusões sobre os dados de forma visual

Nos primeiros 5s a audiência deve saber do que se trata o gráfico

Nos próximos segundos entendem a conclusão.

Fontes:

[1](https://www.ibm.com/br-pt/cloud/learn/exploratory-data-analysis)

[2](https://www.researchgate.net/publication/336778766_Introducao_a_Analise_Exploratoria_de_Dados_com_Python)

[3](https://medium.com/@gabriel.stankevix/analise-explorat%C3%B3ria-de-dados-732007ddbfaf)

[4](https://henriquebraga92.medium.com/estat%C3%ADstica-descritiva-conceitos-b%C3%A1sicos-f715e5ae7fe2)

[5](https://www.aquare.la/o-que-sao-outliers-e-como-trata-los-em-uma-analise-de-dados/)