# Titanic - Machine Learning from Disaster

## 1. Introdução
O desastre do Titanic, em 1912, resultou na morte de 1503 pessoas, tornando-se um dos mais trágicos eventos marítimos da história. Este fato marcou a cultura popular e também se tornou objeto de estudos acadêmicos.

O desafio "Titanic - Machine Learning from Disaster" no Kaggle propõe a tarefa de utilizar aprendizado de máquina para prever quais passageiros sobreviveram ao desastre. O dataset oferecido inclui características como idade, sexo e classe de embarque, sendo amplamente utilizado como exemplo introdutório em cursos de ciência de dados.

O objetivo deste projeto é aplicar técnicas de aprendizado de máquina para prever a sobrevivência dos passageiros do Titanic, além de realizar análise exploratória de dados (EDA), pré-processamento, avaliação do modelo e discussão dos resultados.

## 2. Fundamentação Teórica

### 2.1 Visão Geral de Aprendizado de Máquina
O aprendizado de máquina é um campo da inteligência artificial que permite a detecção automatizada de padrões significativos em dados, capacitando algoritmos a aprender e adaptar-se com base nesses dados.

### 2.1.1 Aprendizado Supervisionado
No aprendizado supervisionado, o algoritmo aprende a mapear entradas para saídas com base em dados rotulados. O desafio do Titanic pode ser abordado como um problema de classificação binária, onde a meta é prever se o passageiro sobreviveu ou não.

### 2.1.2 Árvores de Decisão
Árvores de decisão são classificadores amplamente utilizados, representando alternativas e resultados em forma de árvore. Utilizamos a técnica Random Forest, que combina múltiplas árvores para aumentar a precisão das previsões.

### 2.1.3 Random Forest
O Random Forest é um algoritmo de classificação que utiliza um conjunto de árvores de decisão, atingindo alta precisão. É especialmente eficiente em datasets pequenos ou com valores faltantes, como o desafio do Titanic.

### 2.2 Análise Exploratória de Dados (EDA)
A EDA envolve a análise preliminar de dados utilizando estatísticas e visualizações, buscando insights que ajudem na preparação do dataset e na escolha de modelos adequados.

## 3. Metodologia

### 3.1 Descrição dos Dados
O dataset do Titanic contém 891 entradas para treino e 418 para teste, totalizando 1309. As principais características são:
- **Pclass**: Classe socioeconômica (1a, 2a, 3a classe)
- **Sex**: Sexo (masculino, feminino)
- **Age**: Idade
- **SibSp**: Número de irmãos/cônjuges a bordo
- **Parch**: Número de pais/filhos a bordo
- **Ticket**: Número do bilhete
- **Fare**: Tarifa paga
- **Cabin**: Número da cabine
- **Embarked**: Porto de embarque (C = Cherbourg, Q = Queenstown, S = Southampton)

### 3.2 Pré-processamento de Dados
Os dados faltantes foram tratados da seguinte maneira:
- **Age**: Preenchida com a mediana das idades.
- **Embarked**: Preenchida com a moda.
- **Cabin**: Removida devido à alta porcentagem de valores faltantes.
Além disso, as colunas **Name** e **Ticket** foram eliminadas por não contribuírem com a previsão.

### 3.3 Engenharia de Características
Foi criada a feature **FamilySize**, somando o número de irmãos/cônjuges e pais/filhos + 1. Também foi criada a variável binária **IsAlone** para indicar se o passageiro estava sozinho ou não.

### 3.4 Análise Exploratória de Dados (EDA)
Foram feitas visualizações e análises para verificar a relação entre as características e a sobrevivência. Constatou-se que classe, idade, sexo, tarifa e o fato de estar ou não sozinho são fatores importantes.

![Mapa de Correlação](https://github.com/user-attachments/assets/d30b346e-180d-42e8-ac34-f5cc8de36194)

*Mapa de correlação das características*

![Sobrevivência por Sexo](https://github.com/user-attachments/assets/a1853c0c-1a56-4f67-b3e1-405ccecfe79a)

*Distribuição de sobrevivência por sexo*

![Sobrevivência por Classe](https://github.com/user-attachments/assets/6ef3a99d-d512-4949-a9b0-e61b807f189c)

*Distribuição de sobrevivência por classe*

## 4. Resultados

Para a previsão da sobrevivência, foi treinado um modelo **RandomForestClassifier**. Os hiperparâmetros foram ajustados utilizando validação cruzada e a configuração final foi:
- **n_estimators**: 500
- **max_features**: sqrt
- **max_depth**: 10
- **criterion**: entropy

O modelo atingiu uma precisão de **89.09%** na previsão da sobrevivência dos passageiros.

![Importância das Features](https://github.com/user-attachments/assets/ad4e9a87-652f-440e-8568-552a8b69d145)

*Importância das features no modelo Random Forest*

## 5. Conclusão
O modelo Random Forest apresentou um bom desempenho ao prever a sobrevivência dos passageiros do Titanic. A aplicação de técnicas de engenharia de características e a análise exploratória de dados foram fundamentais para o sucesso do projeto.
