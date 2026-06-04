# NLP e classificação textual aplicados à sugestão de tags em acervos culturais: um estudo com o Met Open Access
MVP de Machine Learning | Pós-Graduação em Data Science & Analytics | PUC-Rio

### Acesse o projeto completo:
[![Open in Colab](https://img.shields.io/badge/Open%20in-Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com/drive/1VWpG1qHCgHeC20rcwfWGXnnmi8cpWWcb?usp=sharing)

## Visão geral
Este projeto investiga a utilização de técnicas de NLP e Machine Learning para apoio à catalogação e sugestão automática de descritores em acervos culturais, utilizando o dataset Open Access do Metropolitan Museum of Art.

## Objetivo
Avaliar a viabilidade de prever descritores a partir dos metadados textuais das obras e explorar relações semânticas entre termos do acervo.
> É possível aprender padrões relevantes nos metadados de um acervo e utilizá-los para sugerir descritores de forma automatizada?

## Fluxo do projeto
Definição do problema → Carga dos dados → Inspeção inicial → EDA → Seleção de variáveis → Pré-processamento → Modelagem → Avaliação → Otimização → Exploração semântica → Interpretação dos resultados

## Principais insights
- Metadados culturais carregam sinais semânticos relevantes para tarefas de classificação textual.
- Muitas previsões incorretas ocorreram entre categorias semanticamente próximas, indicando compreensão parcial do contexto das obras.
- Técnicas clássicas de NLP apresentaram resultados promissores mesmo sem utilização de imagens ou modelos de Deep Learning.
- A combinação entre classificação supervisionada e exploração semântica pode apoiar processos de catalogação e recuperação da informação em acervos culturais.

| Modelo | Acurácia (Teste) | Validação Cruzada |
|----------|----------:|----------:|
| Naive Bayes | 44,0% | 43,1% |
| Logistic Regression | 52,8% | 51,9% |
| LinearSVC | **53,8%** | **53,3%** |

**Modelo selecionado:** LinearSVC  
**Exploração complementar:** Word2Vec (4.746 termos no vocabulário aprendido)  

## Aplicações potenciais
- Sugestão automática de descritores
- Apoio à catalogação
- Revisão de metadados
- Enriquecimento de registros documentais
- Apoio à construção de vocabulários controlados
- Recuperação da informação em acervos digitais 

## Dataset
Conjunto de dados públicos disponibilizados pelo Metropolitan Museum of Art (Met), contendo metadados sobre obras da coleção. 

## Metodologia e tecnologias
Python • Pandas • Scikit-Learn • Plotly • Gensim • Google Colab

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

