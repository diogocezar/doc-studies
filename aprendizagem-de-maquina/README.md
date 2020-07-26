# Aula 01 - Introdução

Aprendizagem de Máquina é uma sub-área de Inteligência artificial. Com início em 1050, tem o principal objetivo de aprender a partir dos dados.

DeepLearning é uma sub-área de Aprendizagem de Máquina, que se popularizou recentemente por conta do poder computacional exigido.

Já, DataSciente tem o foco em áreas como Probabilidade, Estatística, Algebra Linear e a Própria Computação para enteder um grande volumen de dados.

## Por que Agora?

Nunca tivemos tantos dados para serem analisados. Além disso, o poder computacional acessível e uma grande quantidade de ferramentas favorece a utilização de ML.

## O que é?

É a ciência (e arte) de programar computadores de tal forma que eles aprendam a partir de dados [Aurélien Géron, 2017].

## Desafios

Os sistemas inteligentes ainda são muito bons em resolver uma única tarefa. Mas encontram dificuldades quando são retirados de seu contexto original;

## Quando utilizar?

Sempre que não for possível escrever um algoritmo determinístico para resolver o problema. Nesses casos o conhecimento deve ser extraído a partir de exemplos.

O que é um algorítmo determinístico? São algorítmos que dada uma determinada entrada produz uma mesma saída.

OBS. Ao executar um mesmo algoritmo de aprendizagem de máquina, diferentes vezes, pode-se obter resultados diferentes.

## Tipos de Aprendizagem

- Supervisionada: os dados do treinamento estão rotulados;
  - Regressão;
  - Classificação;
- Não supervisionada: os dados não possuem rótulos. Deve-se descobrir estruturas;
  - Clustering;
  - Redução de Dimensionalidade;
- Semi-supervisionada: Uso de dados não rotulados para melhorar a aprendizagem supervisionada.

## Pipeline

1. Obter os dados;
2. Sanitizar, preparar e manipular os dados;
3. Treinar o modelo;
4. Testar o modelo com os dados;
5. Analisar e melhorar os resultados;

## Aprendizagem Supervisionada - Classificação

> Construir um sistema que classifique automaticamente dois tipos de peixe: Salmão e Robalo.

Passos:

1. Dados rotulados: obter características dos dois tipos de peixe, formando a base de treinamento;
2. Representação: deve-se extrair atributos que diferenciem um robalo de um salmão, de forma que sejam similares aos objetos de uma mesma classe e diferentes para objetos de outra classe;
3. Fronteira de decisão: deve-se encontrar uma forma de separar os dois conjuntos. Por exemplo, ao representar os dados em um plano cartesiano, pode-se criar algum tipo de função que separe os 2 conjuntos; Um modelo linear (uma linha que separe os 2 conjuntos) pode não ser bom o suficiente (under-fitting) enquanto que um modelo muito complexo (uma a linha que controen extamente a fronteira entre os conjuntos) não conseguem uma boa generalização, pois decoram a base de treinamento (over-fitting).

## Maldição da Dimensionalidade

Conforme adicionamos características , o número de células cresce de forma exponencial. Por isso, quanto mais características temos, mais base de
dados temos que ter para preencher todas as células.

Por isso é importante ter em mente um equilíbrio das características a serem testada.

## Deep Learning

Utiliza de recursos computacionais, para extrair _automagicamente_ a representação a partir da própria base de Dados.

## Aprendizagem Supervisionada - Regressão

> Construir um sistema para estimar do preço de um imóvel.

Com base em informações de preço e tamanho de diversas casas, a tarefa consiste em estimar o preço de uma dada casa.

Diferentemente da classificação, onde a saída do classificador é
_categórica_, na regressão a saída é um _valor real_.

O modelo mais simples é a regressão linar, mas em alguns casos nem sempre é a melhor solução.

## Aprendizagem não supervisionada

O objetivo é descobrir alguma coisa a respeito dos dados. Por exemplo: como eles estão agrupados.

Trabalha com dados não rotulados, e sua obtenção não é custosa.

Utilizado por exemplo em aplicações de:

- Segmentação de mercado (Marketing);
- Agrupamento de pacientes, clientes, documentos, etc;
- Sistemas de Recomendação;

### Clustering

É a técnica adotada para agrupar os dados em determinados conjuntos.

Desafio: como agrupá-los?

Respostas: definindo bons clusters:

- Compactos e longe um dos outros;

## Redução de Dimensionalidade

A Redução de Dimensionalidade busca identificar e selecionar um subconjunto de características relevantes para um determinado problema, a partir de um conjunto inicial.

Independentemente do algoritmo de aprendizagem de maquina escolhido, um dos principais aspectos na construção de um bom classificador é a utilização de características discriminantes.

A adição de uma nova característica não significa necessariamente um
bom classificador.

Depois de um certo ponto, adicionar novas características pode piorar
o desempenho do classificador.

# Aula 02 - Representação

O objetivo da representação é caracterizar um objeto através de medidas, as quais são bastante similares para objetos da mesma classe, e bastante diferentes para objetos de outras classes.

## Dados Numéricos

É a representação do cenário observado através de sua representação em um vetor de características, como por exemplo:

- Medidas de um sensor;
- Preço de compra;

Mesmo assim, é necessário a realização de operações sobre estes dados, para convertê-los de dados brutos, para catacterísticas. Para isso pode-se aplicar algumas transformações mais básicas e também selecionar as características mais relevantes.

### Transformações Básicas

#### Binatização

É o processo de transformar o conjunto de dados em uma representação binária, no qual 1 representa que o evento aconteceu e 0 representa que o evento não aconteceu.

#### Quantização

Deve-se definir um conjunto de valores representativos para a distribuição do conjunto de dados, e reaplicar cada dado a essa nova classificação.

Por exemplo, se houvessem dados sobre a leitura de valores de 0 a 1. Pode-se definir 4 intervalos: 0 - 0.25 / 0.25 - 0.5 / 0.5 - 0.75 / 0.75 - 1. E para todos os dados, dividívlos nessas categorias.

Assim, se reduz a complexidade do vetor de atributos.

#### Log

Utilização de função Log para melhorar a vizualização de dados que estão concentrados. Ao aplicar a eslaca log, consegue-se uma melhor vizualização desta distribuição.

### Normalização

Por que? Alguns modelos de aprendizagem de máquina são sensíveis a escala
dos dados.

Pode-se utilizar:

- min-max;
- variância;
- l2;

https://en.wikipedia.org/wiki/Feature_scaling

### Seleção de Características

É o procedimento para eliminar características correlacionadas ou pouco discriminantes. Isso reduz a complexidade do modelo, consequentemente o tempo de
aprendizagem.

Não é trivial, pois para encontrar o melhor conjunto de características, todas as combinações devem ser testadas.

## Texto

Diversas aplicações, como por exemplo, classificação de texto, recuperação de informação, agrupamento e organização de documentos, identificação de autoria, etc. Algoritmos de aprendizagem de máquina não trabalham com texto
diretamente, ou seja, o texto deve ser convertido em números.

### Bag of Words

É uma estratégia simples e flexível para representar os textos que envolve 2 passos:

- Definir um vocabulário conhecido;
- Quantificar a presença de palavras conhecidas;

#### TF-IDF

Um problema com a simples frequência de palavras é que algumas delas podem dominar o documento, mas não necessariamente conter informação discriminante.

Uma solução é normalizar a frequência de palavras pela quantidade
que elas aparecem no documento.

#### Limitações

- Definição cuidadosa do vocabulário (tamanho)
- Falta de contexto (old bike vs used bike);

### Word Embedding

O modelo Word2Vec é baseado em uma rede neutal. Seu treinamento é baseado em pares de palavras extraídos do texto.

Isso faz com que o contexto seja considerado nos resultados apresentados pelo modelo.

## Imagens

### Momentos de Hu

Permite a identificação de padrões com base em 7 momentos invariantes.

### Características Estruturais

Extraem informações da estrutura do padrão.

- Contornos;
- Concavidades;
- Esqueleto;
- Perfil;
- Área, Distribuição;

Muitas vezes informações estatísticas são computadas a partir das
informações estruturais.

#### Concavidades

Obter informações estruturais com base nas concavidades do objeto. Baseia-se na quantidade de vizinhos pretos em n-direções.

#### Contorno

Para cada pixel do contorno, contabiliza-se a direção do próximo pixel.

#### Histogramas de Projeção

Nesse caso podemos usar um histograma para representar a distribuição
dos pixels da imagem.

#### Zoneamento

Zoneamento é uma estratégia bastante usada para enfatizar determinadas regiõees de um padrão.

#### Textura

Padrão visual que possui algumas propriedades de homogeneidade que não resultam simplesmente de uma cor ou intensidade.

#### Gradientes

Imagens de gradientes geralmente são produzidas através da convolução de filtros pré-determinados em imagens.

# Aula 03 - Funções de Custo, Reamostragem e Avaliação de Classificadores

São os principais problemas que temos com os dados:

- Dados faltantes
- Dados desbalanceados
- Variáveis correlacionadas
