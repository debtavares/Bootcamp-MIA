<h1> Regressão e Classificação de dados </h1>

**Conceitos:**

**Regressão**: prever um valor baseado em dados históricos conhecidos.

## **Aprendizado de máquina**

É prever os resultados com base nos dados recebidos.

Quanto maior a variedade de amostras, mais fácil será encontrar padrões relevantes para prever um resultado. Portanto, precisamos de três componentes para ensinar a máquina:

- **Dados**:

Deseja detectar spam? Obtenha amostras de mensagens de spam. 

Quer prever estoques? Encontre o histórico de preços. 

Quer descobrir as preferências de um usuário? Analise suas atividades no Facebook.

- **Características/Features:**

Também conhecidos como parâmetros ou variáveis.

São os fatores aos quais a máquina vão analisar, como os nomes das colunas em uma tabela.

- **Algoritmos:**

O método escolhido afeta a precisão, o desempenho e o tamanho do modelo final.

- **Variável independente ou preditora:**

É aquela que será passada para o modelo, tendo influência na variável que queremos encontrar. Por exemplo: Se queremos prever as vendas de sorvete, a estação do ano pode interferir nas vendas.

- **Variável alvo ou dependente:**

É a variável que queremos prever. No exemplo acima seria as vendas de sorvete.

**Inteligência artificial** é o nome de todo um campo de conhecimento.

**Aprendizado de Máquina** é uma parte da inteligência artificial. 

**Redes neurais** são um dos tipos de aprendizado de máquina. 

**Deep Learning** é um método moderno de construção, treinamento e uso de redes neurais. Basicamente, é uma nova arquitetura. Hoje em dia, na prática, ninguém separa a deep learning das “redes mais comuns”. Nós até usamos as mesmas bibliotecas para elas. 



## **Aprendizagem supervisionada:**

- Possui um “professor” que dá a maquina todas as respostas;
- É aplicado quando tenta encontrar a relação entre a variável de alvo e as variáveis independentes;
- É onde você tem variáveis de entrada (x) e uma variável de saída (Y) e você usa um algoritmo para aprender a função de mapeamento da entrada para a saída **Y = f (X)**. O objetivo é aproximar a função de mapeamento tão bem que, quando você tiver novos dados de entrada (x), você possa prever as variáveis de saída (Y) para esses dados.

Requer que os dados usados para treinar o algoritmo já estejam rotulados com as respostas corretas, ou seja, nos dados de treino eu preciso ter os dados anotados com o valores corretos e nós sabemos do resultado de saída. A máquina aqui é como um bebê aprendendo a classificar brinquedos: aqui está um robô, aqui está um carro, aqui está um carro-robô …

Existem dois tipos: **classificação** (predição de categoria) e **regressão** (predição de um ponto específico em um eixo numérico).

### **Classificação:**

Dividem os objetos com base em um dos atributos conhecidos de antemão. 

Separa as meias com base na cor, documentos baseados na linguagem e as músicas por gênero.


**Usada nos dias de hoje para:**

- Filtragem de spam;
- detecção de idioma;
- Pesquisa por documentos semelhantes;
- Análise de sentimentos;
- Reconhecimento de caracteres e números manuscritos;
- Detecção de fraude.

Algoritmos populares:

[Naive Bayes](https://www.datageeks.com.br/naive-bayes/),
[Decision Tree](https://en.wikipedia.org/wiki/Decision_tree_learning),
[Logistic Regression](https://en.wikipedia.org/wiki/Logistic_regression),
[K-Nearest Neighbours](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm),
[Support Vector Machine](https://en.wikipedia.org/wiki/Support_vector_machine)

- **Naive Bayes**

Amplamente utilizado na filtragem de spam, mas outros algoritmos são preferíveis.

Ele recebe o nome de “naive” (ingênuo) porque desconsidera a correlação entre as variáveis (features). Ou seja, se determinada fruta é rotulada como “Limão”, caso ela também seja descrita como “Verde” e “Redonda”, o algoritmo não vai levar em consideração a correlação entre esses fatores. Isso porque **trata cada um de forma independente.**

Ou seja, o teorema de Bayes trata sobre **probabilidade condicional.** Isto é, qual a probabilidade de o evento A ocorrer, dado o evento B.

Um problema simples que exemplifica bem o teorema é o cálculo de probabilidades em cima de diagnóstico de doenças.

Imagine que estamos trabalhando no diagnóstico de uma nova doença. Após realizar testes, coletas e análises, descobrimos que:

**100** pessoas realizaram o teste.

**20%** das pessoas que realizaram o teste possuíam a doença.

**90%** das pessoas que possuíam a doença, receberam positivo no teste.

**30%** das pessoas que não possuíam a doença, receberam positivo.

A partir destes dados, surge o problema: se uma nova pessoa realizar o teste e receber um resultado positivo, qual a probabilidade dela realmente possuir a doença?

Para isso, é preciso multiplicar a probabilidade *a priori* (possuir a doença) pela probabilidade de “receber um resultado positivo, dado que tem a doença”.

Com esses dados, também podemos calcular a probabilidade *a posteriori* da negação (não possuir a doença, dado que recebeu um resultado positivo).

P(doença|positivo) = 20% * 90%

P(doença|positivo) = 0,2 * 0,9

P(doença|positivo) = 0,18

P(não doença|positivo) = 80% * 30%

P(não doença|positivo) = 0,8 * 0,3

P(não doença|positivo) = 0,24

Finalizado o cálculo inicial, é preciso normalizar os dados, para que a soma das duas probabilidades resulte 100% ou 1. Para gerar os dados normalizados dividimos o resultado pela soma das duas probabilidades.

**Exemplo:**

P(doença|positivo) = 0,18/(0,18+0,24) = 0,4285

P(não doença|positivo) = 0,24/(0,18+0,24) = 0,5714

0,4285 + 0,5714 = 0,9999.. (ou aproximadamente 1)

- **Árvore de decisão**

Vamos dizer que você precisa de algum dinheiro a crédito. Como o banco saberá se você vai pagá-lo de volta ou não? Não há como saber com certeza. Mas o banco tem muitos perfis de pessoas das quais recebeu dinheiro antes. 

Usando esses dados, podemos ensinar a máquina a encontrar padrões e obter a resposta. Entretanto, o banco não pode confiar cegamente na resposta da máquina.

Para lidar com isso, temos as árvores de decisão. Todos os dados são automaticamente divididos em perguntas de sim ou não.

Árvores de decisão puras raramente são usadas hoje. No entanto, elas frequentemente estabelecem a base para grandes sistemas e seus conjuntos até funcionam melhor que redes neurais.

- **Regressão Logística**
- **K-nearest neighbors algorithm (KNN)**

A predição é feita comparando o dado com os **k** dados de treinos mais próximos.

O dado novo é classificado com a classe mais comum.

Como definir **k**?

Testando vários valores para **k**!

O que der o menor erro será o **k**.

- **Support-vector machine (SVM)**

Foi usado para classificar tudo o que existe: plantas por aparência em fotos, documentos por categorias, etc.

A ideia por trás do SVM é simples – ele tenta desenhar duas linhas entre seus pontos de dados com a maior margem entre eles. Veja a imagem abaixo:

Usado na detecção de anomalias. Quando um recurso não se encaixa em nenhuma das classes, nós o realçamos.

Os mercados de ações também utilizam ela para detectar um eventual comportamento anormal dos comerciantes para encontrar os *insiders*. Ao ensinar um computador as coisas certas, nós automaticamente ensinamos quais são as coisas que estão erradas.

Atualmente, as redes neurais são mais freqüentemente usadas para classificação. Alias, é para isso que elas foram criadas…

**A regra geral é quanto mais complexos os dados, mais complexo é o algoritmo.**
 Para textos, números e tabelas, eu escolheria a abordagem clássica. Os modelos são menores lá, eles aprendem mais rápido e trabalham com mais clareza. Para fotos, vídeos e todas as outras coisas complicadas de Big Data, eu definitivamente optaria por redes neurais.

### Regressão

**Usada nos dias de hoje para:**

- Previsões do preço das ações;
- Análise de demanda e volume de vendas;
- Diagnóstico médico;
- Quaisquer correlações numéricas.

Algoritmos populares: [Regressão Linear](https://en.wikipedia.org/wiki/Linear_regression) e [Regressão Polinomial](https://en.wikipedia.org/wiki/Polynomial_regression).

Regressão é basicamente uma classificação em que prevemos um número em vez de uma categoria. Exemplos disso são a previsão do preço de um carro pela sua quilometragem, tráfego por hora do dia, volume de demanda por crescimento da empresa, etc. A regressão é perfeita quando algo depende do tempo.

Quando a linha resultante é reta – é uma regressão linear, quando é curva – polinomial. Esses são os dois tipos principais de regressão. Os outros são mais exóticos. A regressão logística é uma excessão, pois não é uma regressão, mas sim um método de classificação. Fique atento!

**Regressão Linear**

Regressão linear é um algoritmo supervisionado de machine learning usado para estimar o valor de algo baseado em uma série de outros dados históricos, portanto olhando para o passado você pode “prever” o futuro.

Existem 2 tipos de regressão linear: simples e a múltipla.

**Regressão linear simples :** refere-se quando temos somente uma variável independente (X) para fazermos a predição.

**Regressão linear múltipla:** refere-se a várias variáveis independentes (X) usadas para fazer a predição.

Esse algoritmo pode ser utilizado em qualquer problema, onde as variáveis de entrada e saída são valores contínuos. Por exemplo:

· Prever as vendas de um determinado produto

· Setor imobiliário (valor de um imóvel)

· Calcular a expectativa de vida de um país

· Calcular a pressão sanguínea de um paciente

Esse tipo de algoritmo é aplicado quando há uma boa correlação linear (positiva ou negativa) entre os dados, ou seja, quando o relacionamento ou associação entre os dados pode ser definido com uma reta.

- **Mas o que é correlação?**

É uma medida estatística utilizada para calcular a associação entre os pontos.

**Correlação Linear de Pearson:** mede a correlação linear entre a nuvem de pontos. O resultado varia entre -1 e 1:

1: Correlação linear perfeita negativa

1: Correlação linear perfeita positiva

0: Não tem correlação **linear**

Uma forma mais fácil de selecionar as variáveis independentes para o modelo de regressão é calcular a correlação entre elas e a variável alvo.

No exemplo acima, queremos prever a nota de matemática (NU_NOTA_MT) do enem. Para isso, vamos utilizar as colunas com alta correlação com a variável alvo. 

E com isso podemos selecionar as seguintes variáveis: ‘NU_NOTA_CN’,’ NU_NOTA_CH’, ’NU_NOTA_LC’, ’NU_NOTA_REDACAO’.

## **Aprendizagem não supervisionada:**

A máquina é deixada sozinha com uma pilha de fotos de animais e uma tarefa: descobrir quem é quem. Os dados não são rotulados, não há professor e a máquina está tentando encontrar padrões por conta própria.

### Clusterização

“Divide objetos com base em características desconhecidas. A máquina escolhe o melhor caminho”.

**Usada nos dias de hoje para:**

- Segmentação de mercado (tipos de clientes, fidelidade);
- Mesclar pontos próximos em um mapa;
- Compressão de imagem;
- Analisar e rotular novos dados;
- Detectar um comportamento anormal.

Algoritmos populares: [K-means_clustering](https://en.wikipedia.org/wiki/K-means_clustering), [Mean-Shift](https://en.wikipedia.org/wiki/Mean_shift), [DBSCAN](https://en.wikipedia.org/wiki/DBSCAN).

É uma classificação sem classes predefinidas. É como dividir meias por cor quando você não se lembra de todas as cores que você tem.

### Feature Engineering

Etapa crucial paracriação de modelos de ML;

Feita junto com a Análise Exploratória de dados (EDA).

Algumas coisas que podem ser feitas nessa etapa são:

- Tratamento de valores faltantes;
- Tratamento de outliers;
- Normalização de dados;
- Criação de variáveis.

Finalizada essa etapa, temos o conjunto de dados para a modelagem. Mas antes é preciso separar o conjunto de dados em 2:

- **Conjunto de treinamento**: utilizado pelo modelo para aprender;
- **Conjunto de teste**: utilizado para avaliar o desempenho do modelo para dados não vistos.

### **Como iniciar um projeto com Aprendizado de Máquina?**

Logo abaixo podemos ver o passo a passo (***pipeline***) que podemos tomar ao iniciar um projeto:

- **Entendimento do problema:** Entendemos o problema, entrevistamos a pessoa cliente, identificamos qual dor queremos resolver e como poderemos ajudar a sanar ou a melhorar esse problema. Essa etapa é essencial para toda a *pipeline* que iremos executar, pois sem o entendimento do negócio, o modelo que faremos não vai ter utilidade para clientes finais. **Após isso é realizado a coleta dos dados.** Então, precisamos pensar o seguinte nesta etapa: Por qual caminho vou coletar meus dados? É via API? É via banco de dados?
- **Entendimento dos dados:** A partir de exploração, conseguimos entender qual o comportamento do dado, qual a distribuição, qual o tipo de dado (se ele é estruturado ou não estruturado), se há *[outliers](https://medium.com/ensina-ai/outlier-o-ponto-fora-da-curva-1f28f3d9c23)* (dados com valores atípicos) no dataset e por aí vai. Com essa exploração conseguimos entender qual o tipo de algoritmo podemos aplicar e também nesta etapa pode ser verificado se esses dados são o suficiente para chegar na solução do problema da pessoa cliente.
- **Análise exploratória:** assim como fazer um bolo, é preciso validar se há todos os ingredientes necessários antes de começar. Para saber mais sobre isso, clique [aqui.](https://www.kaggle.com/ekami66/detailed-exploratory-data-analysis-with-python)
- **Limpeza e pré-processamento:** se no dataframe explorado tiver *outliers* eu os removo se necessário. Além disso, precisamos validar se tem dados faltantes, se houver, informar para a pessoa cliente que está faltando esses dados. Também é importante verificar se as colunas estão com o tipo certo, por exemplo: se o dataframe tem uma coluna de idade, faz sentido ela ser do tipo “float”? Para saber mais sobre pré-processamento, clique [aqui.](https://www.kaggle.com/furtadobb/2-pre-processamento-de-dados-done)
- **Treinar o modelo:** Antes de passar os dados para o modelo, é recomendado ter pelo menos 2 datasets: um de teste e outro de treino. Eu recomendo dividir sua base em 20% para teste e 80% para treino. Os dados de treino deverão ser passados como input para o modelo realizar o treino. Essa etapa é bem importante pois assim além de treinar, é necessário saber o quanto seu modelo performa com dados que ele não conhece.
- **Testar e avaliar os resultados gerados:** O procedimento mais comum após treinar um modelo de Machine Learning é testá-lo para que saibamos se o modelo é capaz de generalizar bem para novos dados, onde é passado como input pro modelo os dados que ele nunca viu antes. As métricas são usadas para avaliar se o modelo está “bom” ou “ruim”, ou seja, se o modelo consegue se adaptar à novos dados. Para saber mais, clique [aqui](https://paulovasconcellos.com.br/como-saber-se-seu-modelo-de-machine-learning-est%C3%A1-funcionando-mesmo-a5892f6468b). Caso o resultado não seja bom, precisa ser reavaliado os parâmetros e verificar se os dados que você está usando realmente são necessários. E caso os resultados sejam bons, você pode entregar o modelo para a pessoa cliente.

Fontes:

[1]([https://www.datageeks.com.br/machine-learning/](https://www.datageeks.com.br/machine-learning/))

[2](https://medium.com/@lauradamaceno/regress%C3%A3o-linear-6a7f247c3e29)