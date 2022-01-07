# **Apache Spark: Uma breve introdução**



##  **História **

Lidar com grande volume de dados costumava ser uma tarefa praticamente impossível a pouco mais de uma década uma vez que não tinhamos tanto poder computacional e plataformas de processamento paralelo ainda não eram realidade, contudo com a criação do [Hadoop](https://www.dtidigital.com.br/blog/hadoop/) surgiu uma  ferramenta que resolvia os 3 grandes problemas da computação paralela sendo:

* A paralelização (como performar subsets simultaneamente)
* Distribuição (como distribuir os dados)
* E tolerancia a falha (como lidar falha de componente)

Por certo tempo o Hadoop dominou o mercado de Big Data, mas ainda haviam muitos problemas que não poderiam ser resolvidos e diversas ferramentas foram criadas usando-o como base mas ainda sem um padrão o que tornou difícil sua utilização. Em 2009 a AmpLab lança a primeira versão do Spark que em 2013 seria então assumida pela Apache Software Foundation.

Segundo o criador do Spark, Matei Zaharia, podemos defini-lo como uma ferramenta computação paralela que generalisa o modelo de programação do MapReduce, aproveitando assim todos as vantagens já implementadas pelo Hadoop e desenvolvendo melhorias como veremos a seguir.

## **Arquitetura básica**

Podemos enteder o Spark como uma evolução do Hadoop e do paradigma de programação Map-Reduce, podendo ser de 10 a 100 vezes mais rápido graças ao seu uso eficiente da memória que não persiste os dados em discos enquanto está realizando seu processamento. 

O Spark é atualmente criado em Scala rodando sobre a JVM - Java Virtual Machine, contudo podemos usar 5 linguagens para desenvolver sendo Scala, Java, SQL, Python e R.

Além disso ao ser desenvolvido uma grande preocupação foi a criação de uma API que fosse capaz de gerenciar todo o paralelismo de modo que o desenvolver final pudesse ter a impressão de estar trabalhando apenas com um computador e pudesse de fato forcar esforços em suas tarefas seja de transformação, analise ou ainda outras. 

É possível ter uma ideia de como o Spark está organizado pelo seguinte diagrama:

![Camadas de arquitetura do Apache Spark](/home/vitor/dti/codigos/Projetos-EngDados/SparkArchitecture.png)

### Low Level API's

Este nível contém as funcionalidades basicas para rodar jobs e outras  funcionalidades requeridas pelos demais componentes. É nela também que se define o conceito de RDD - Resilient distributed dataset, uma abstração da coleção de dados que foi distribuida. 

Outras funções importantes desta camada são o gerenciamento de segurança, rede, agendamento e ainda o acesso logico a sistemas de arquivos HDFS, GlusterFS, Amz S3 e demais.

### Structured API's

Já o nível de Structured API trabalha a manipulação dos dados seja por meio dos DataSets ou dos DataFrames (a diferença entre os dois está na tipagem que será prédefinida e checada no caso dos DataSets enquanto no DataFrame somente haverá uma checagem entre as linhas) que podem ser lidos de diversos formatos como Hive, Parquet, JSON e outros ainda. Utilizando o SparkSQL (API que nos permite escrever querys em SQL) podemos manipular os dados da forma como desejamos e ainda com a ajuda do Catalyst possuimos um otimizador de query trazendo mais eficácia.

### High Level

No nível mais alto temos o ecossistema Spark com suas diversas bibliotecas incluido Spark Streaming, Spark MLlib e Spark GraphX, que são responsáveis respectivamente por cuidar de ingestão em streaming (seja por HDFS, Kafka...) e os processos ao redor como recuperação de falhas; Criar e validar modelos clássicos de machine learning; e por útlimo lidar com grafos e seus algoritmos.

##  **Pra quem é o Spark?**

Graças ao seu suporte para 5 linguagens de desenvolvimento a utilização do Spark pode ser de fácil adoção por todo o time de dados. Vejamos com mais detalhes:

* Engenheiro de Dados: Poderá utilizar o spark para o processo de extração, transformação e carga dos dados (ETL/ELT/EL), sendo que os processos podem ser em batch ou streaming;
* Cientistas de Dados: Por meio de bibliotecas como SparkML ou Spark GraphX o profissional poderá aplicar modelos de ML;
* Analistas de Dados: Para o analista de dados todo o poder do SparkSQL poderá ser utilizado para gerar relatórios e insights sobre todo o volume de dados de forma otimizada graças ao Catalyst.

Vale dizer que com o uso combinado entre Spark e [Databricks](https://databricks.com/#) o desenvolvimento de programas fica ainda mais simples podendo ainda ser intregado com grandes serviços de nuvem como Azure, AWS e GCP.

Quer descobrir se o Spark pode ser úitl pra você? Então fale com  a DTI. Estamos abertos a tirar dúvidas e criar uma solução que gere valor ao seu negócio! Além disso podemos mostrar como o agilismo e a trasnformação digital pode facilitar processos dentro da sua empresa! 

No podcast[ Os Agilistas](https://osagilistas.com/) você confere de perto a percepção dti sobre o agilismo e como aplicá-lo de maneira eficiente um uma equipe. Te esperamos lá! E se você tem  interesse em fazer parte de um time que entende de cultura agil e te dá a oportunidade de trabalhar com Spark na prática, [se inscreva em nossa página de carreiras](https://www.dtidigital.com.br/venha-ser-dti/) e venha ser dti!



