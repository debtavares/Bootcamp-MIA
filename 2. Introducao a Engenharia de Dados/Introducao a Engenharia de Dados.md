<h1> Engenharia de dados </h1>

Engenharia de dados é a combinação de conhecimentos e práticas para implementar mecanismos de **coleta, tratamento, processamento e armazenamento de dados**.

Ela cria a estrutura do banco de dados e disponibiliza para quem precisa consumir.

Dados podem ser:

- **Estruturados**: Dados relacionados, como em tabela.
- **Semi estruturado**: Quando estão em formato em Json, XML.
- **Não estruturados**: São os vídeos, imagens.

Existem muitos **tipos de estruturas**, mas as quatro principais são:

- listas;
- árvores;
- grafos;
- Tabelas Hash

Os pontos a seguir destacam as diferenças entre dados estruturados vs. dados não estruturados vs. dados semiestruturados:

- **Organização:** Os dados estruturados são bem organizados; portanto, possui o mais alto nível de organização, enquanto os dados semiestruturados são parcialmente organizados; portanto, o nível de organização é menor do que o dos dados estruturados, mas maior do que o dos dados não estruturados. Por último, esta última categoria não está organizada.
- **Flexibilidade e escalabilidade:** Os dados estruturados são bancos de dados relacionais ou dependentes de esquema, portanto, menos flexíveis e difíceis de escalar, enquanto os dados semiestruturados são mais flexíveis e mais simples de escalar do que os dados estruturados. No entanto, os dados não estruturados não têm um esquema que os torna mais flexíveis e escalonáveis em relação aos outros dois.
- **Controle de versão:** Como os dados estruturados são baseados em um banco de dados relacional, o controle de versão é executado em tuplas, linhas e tabelas. Por outro lado, em dados semiestruturados, tuplas ou gráficos são possíveis, pois apenas um banco de dados parcial é suportado. Por fim, em dados não estruturados, o controle de versão é provavelmente um dado completo, pois não há suporte de banco de dados.
- **Gestão de transações:** Em dados estruturados, a simultaneidade de dados está disponível e, portanto, geralmente preferida para o processo multitarefa. Enquanto em dados semiestruturados, a transação é adaptada do DBMS, mas ainda assim, a simultaneidade de dados não está disponível. Por último, em dados estruturados, nem o gerenciamento de transações nem a simultaneidade de dados estão presentes.

Qualidade dos dados (o quão confiáveis são):

- **Singularidade**: Verificar se o dado é igual ao dataset, se não possui dados duplicados;
- **Completude**: Garantir que as informações sejam completas, não deixem de lado informações relevantes;
- **Pontualidade**: Garantir que a ocorrência dos eventos sejam em tempo real.
- **Validade**: Representa o nível em que os dados estão de acordo com sua definição – formato, tipo, faixa de valores
- **Acurácia**: Avalia a veracidade dos dados;
- **Consistência**: Mesmo que o registro e dados seja feito em locais diferentes, os dados devem ser iguais
.

**Papel da pessoa Engenheira de Dados:**

Gerencia e organiza os dados. Trata os dados brutos para disponibilizar com mais qualidade.

<h2>Business Intelligence</h2>

Inteligência de Negócios. É conjunto de processos que possibilita transformar dados em informações extremamente relevantes.

Etapas:

- Reunir as fontes dos dados;
- ETL (Extrair, transformar e carregar), ou seja, extrair os dados de todas as fontes selecionadas e transformá-los de forma que permita a comunicação entre os dados de diferentes áreas e também para limpar as “sujeiras” armazenadas.
- Estruturação das tabelas em um Data Warehouse;
- Visualização dos dados (Power BI).

<h2>Data Lake, Data Warehouse e Lakehouse</h2>

- A indústria de tecnologia tem buscado formas eficientes para armazenar e analisar grandes volumes de dados.

**Data Warehouse:**

- Armazenamento centralizado de informações que podem ser explorados;
- Contêm grandes quantidades de dados históricos;
- Usado para análises sobre os dados estruturados pelo BI.

**Data Lake:**

- Armazena todos os tipos de dados (estruturados, semiestruturados e não estruturados);
- Se mantém em formato bruto até que estejam prontos para uso;
- Os dados são transformados apenas quando são necessários para análises, por meio da aplicação de esquemas;
- Explorados pelos cientistas de dados e BI.

**Data Lakehouse:**

- Centralizar e unificar as fontes de dados e esforços de engenharia na organização;

Fontes:

[Dado estruturado e semi estruturado](https://www.astera.com/pt/type/blog/structured-semi-structured-and-unstructured-data/](https://www.astera.com/pt/type/blog/structured-semi-structured-and-unstructured-data/)

[Business Inteligence](https://www.alura.com.br/artigos/business-intelligence-o-que-e](https://www.alura.com.br/artigos/business-intelligence-o-que-e)

[Ladekouse: unindo o Data Lake e o Data Warehouse](https://medium.com/data-hackers/lakehouse-unindo-o-data-lake-e-o-data-warehouse-1428be2dda21)