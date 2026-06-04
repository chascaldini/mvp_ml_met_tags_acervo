# NLP e classificação textual para apoio à catalogação e sugestão de descritores em acervos culturais: um estudo com o Met Open Access
MVP de Machine Learning aplicado a acervos culturais | Pós-Graduação em Data Science & Analytics | PUC-Rio

### Acesse o projeto completo:
[![Open in Colab](https://img.shields.io/badge/Open%20in-Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com/drive/1VWpG1qHCgHeC20rcwfWGXnnmi8cpWWcb?usp=sharing)

## Visão geral
Este projeto investiga a utilização de técnicas de NLP e Machine Learning para apoio à catalogação e sugestão automática de descritores em acervos culturais, utilizando o dataset Open Access do Metropolitan Museum of Art.

## Objetivo
Avaliar a viabilidade do uso de técnicas de NLP e Machine Learning para apoiar a sugestão automática de descritores a partir dos metadados textuais de obras e objetos culturais.
> É possível aprender padrões relevantes nos metadados de um acervo e utilizá-los para sugerir descritores de forma automatizada?

## Fluxo do projeto
Definição do problema → Carga dos dados → Inspeção inicial → EDA → Seleção de variáveis → Pré-processamento → Modelagem → Avaliação → Otimização → Exploração semântica → Interpretação dos resultados

## Dataset
Conjunto de dados públicos disponibilizados pelo [Metropolitan Museum of Art (Met)](data/), contendo metadados sobre obras da coleção.

## Abordagem utilizada
Python • Pandas • Scikit-Learn • Plotly • Gensim • Google Colab

## Desempenho dos modelos
| Modelo | Acurácia (Teste) | Validação Cruzada |
|----------|----------:|----------:|
| Naive Bayes | 44,0% | 43,1% |
| Logistic Regression | 52,8% | 51,9% |
| LinearSVC | **53,8%** | **53,3%** |

**Modelo selecionado:** LinearSVC  
**Exploração complementar:** Word2Vec (4.746 termos no vocabulário aprendido)  

## Principais insights

- Os metadados textuais do acervo contêm informações suficientes para apoiar a previsão automática de descritores, mesmo sem utilização das imagens das obras.
- Grande parte dos erros ocorreu entre categorias semanticamente próximas, sugerindo que os modelos frequentemente capturam o contexto geral do objeto cultural.
- Modelos clássicos de NLP baseados em TF-IDF apresentaram resultados consistentes em uma base com mais de 155 mil registros e 100 categorias distintas.
- A exploração com Word2Vec revelou relações semânticas coerentes entre termos do acervo, indicando potencial para aplicações futuras em sugestão de descritores e vocabulários controlados.
- Os resultados reforçam a viabilidade do uso de NLP e Machine Learning como ferramentas de apoio à catalogação e recuperação da informação em acervos culturais.

## Aplicações em acervos culturais
- Sugestão automática de descritores
- Apoio à catalogação
- Revisão de metadados
- Enriquecimento de registros documentais
- Apoio à construção de vocabulários controlados
- Recuperação da informação em acervos digitais 

## Notebook do projeto
O notebook completo pode ser acessado pelo botão no topo deste repositório.

## Como executar
1. Acessar o notebook pelo botão **Open in Colab**
2. Executar todas as células do início ao fim
3. Acompanhar a narrativa do notebook, incluindo EDA, modelagem, avaliação dos modelos e exploração semântica com Word2Vec.

## Autora
Charlyne Scaldini  
[LinkedIn](https://www.linkedin.com/in/charlyne-scaldini-92959a2b2)  
chascaldini@gmail.com

