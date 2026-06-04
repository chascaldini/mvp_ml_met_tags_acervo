# NLP e classificação textual aplicados à sugestão de tags em acervos culturais: um estudo com o Met Open Access
MVP de Machine Learning | Pós-Graduação em Data Science & Analytics | PUC-Rio

### Acesse o projeto completo:
[![Open in Colab](https://img.shields.io/badge/Open%20in-Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com/drive/1VWpG1qHCgHeC20rcwfWGXnnmi8cpWWcb?usp=sharing)

## Visão geral
Acervos culturais costumam reunir milhares de registros documentais, fotográficos e museológicos descritos por meio de metadados textuais. A atribuição de descritores e palavras-chave é uma atividade fundamental para a recuperação da informação, mas pode demandar tempo, conhecimento especializado e grande esforço de catalogação.

Este projeto investiga como técnicas de Processamento de Linguagem Natural (NLP) e Machine Learning podem apoiar a sugestão automática de descritores a partir dos próprios metadados de um acervo.

Para isso, foi utilizado o dataset Open Access do Metropolitan Museum of Art (The Met), contendo informações sobre obras, objetos e coleções culturais.

## Objetivo
Avaliar a viabilidade do uso de técnicas de NLP para apoiar processos de catalogação e indexação em acervos culturais por meio da classificação textual de descritores.

O projeto busca responder à seguinte questão:

> É possível aprender padrões relevantes nos metadados de um acervo e utilizá-los para sugerir descritores de forma automatizada?

## Resultados

O LinearSVC apresentou o melhor desempenho geral, sendo selecionado como modelo principal do projeto.

Além da classificação supervisionada, a exploração com Word2Vec demonstrou a capacidade de identificar relações semânticas coerentes entre termos do acervo, sugerindo aplicações futuras relacionadas à recomendação de descritores e apoio à construção de vocabulários controlados.

## Principais insights
- Metadados culturais carregam sinais semânticos relevantes para tarefas de classificação textual.
- Muitas previsões incorretas ocorreram entre categorias semanticamente próximas, indicando compreensão parcial do contexto das obras.
- Técnicas clássicas de NLP apresentaram resultados promissores mesmo sem utilização de imagens ou modelos de Deep Learning.
- A combinação entre classificação supervisionada e exploração semântica pode apoiar processos de catalogação e recuperação da informação em acervos culturais.

## Aplicações potenciais
- Sugestão automática de descritores
- Apoio à catalogação
- Revisão de metadados
- Enriquecimento de registros documentais
- Apoio à construção de vocabulários controlados
- Recuperação da informação em acervos digitais 

## Dataset
Conjunto de dados públicos disponibilizados pelo Metropolitan Museum of Art (Met), contendo metadados sobre obras da coleção. 

Principais características da base utilizada:

* 192 mil registros com Tags disponíveis
* 155 mil registros após filtragem para modelagem
* 100 Tags principais mais frequentes
* Metadados textuais provenientes de títulos, materiais, tipologias e classificações institucionais

## Metodologia e tecnologias

**Preparação dos dados**
- Análise exploratória de dados (EDA)
- Seleção de features textuais
- Construção de campo textual combinado
- Limpeza textual
- Vetorização com TF-IDF
- Pipeline com prevenção de data leakage

**Modelagem**

Modelos avaliados:
- Naive Bayes (baseline)
- Logistic Regression
- LinearSVC

Avaliação:
- Train/Test Split
- Validação Cruzada
- Classification Report
- Matriz de Confusão
- Análise qualitativa de erro

**Exploração semântica complementar**
- Word2Vec
- Similaridade entre termos
- Relações semânticas em metadados culturais

**Ferramentas**
Python  
Pandas  
NumPy  
Scikit-Learn  
Plotly  
Gensim  
Google Colab  

## Notebook do projeto
O notebook completo pode ser acessado pelo botão no topo deste repositório.

## Como executar

1. Acessar o notebook pelo botão **Open in Colab**
2. Executar todas as células do início ao fim
3. Explorar as análises e visualizações

## Autora
Charlyne Scaldini  
[LinkedIn](https://www.linkedin.com/in/charlyne-scaldini-92959a2b2)  
chascaldini@gmail.com

