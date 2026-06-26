# Classificação textual e técnicas de NLP para apoio à catalogação e sugestão de descritores em acervos culturais: um estudo com o Met Open Access
MVP de Machine Learning | Pós-Graduação em Data Science & Analytics | PUC-Rio

### Acesse o projeto completo:
[![Open in Colab](https://img.shields.io/badge/Open%20in-Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com/drive/1VWpG1qHCgHeC20rcwfWGXnnmi8cpWWcb?usp=sharing)

## O desafio
Descritores são elementos fundamentais para a organização, recuperação e descoberta de informações em acervos culturais. Mas será que é possível identificar padrões nos próprios metadados das obras e utilizá-los para apoiar a sugestão automática desses descritores?

Este projeto explora essa questão por meio de técnicas de Machine Learning e Processamento de Linguagem Natural (NLP), utilizando o dataset Open Access do Metropolitan Museum of Art (The Met). A proposta é investigar até que ponto informações presentes em campos como título, material, tipologia e contexto institucional podem contribuir para processos de catalogação e indexação assistidos por inteligência artificial.

> É possível aprender padrões relevantes nos metadados de um acervo e utilizá-los para sugerir descritores de forma automatizada?

## Fluxo do projeto
Definição do problema → Carga dos dados → Inspeção inicial → EDA → Seleção de variáveis → Pré-processamento → Modelagem → Avaliação → Otimização → Exploração semântica → Interpretação dos resultados

## Abordagem metodológica
**Técnicas:** NLP • TF-IDF • Classificação supervisionada • Validação cruzada • Otimização de hiperparâmetros • Word2Vec  
**Modelos avaliados:** Multinomial Naive Bayes (baseline), Logistic Regression e LinearSVC.  
**Tecnologias:** Python, Pandas, Scikit-Learn, Plotly, Gensim e Google Colab.  

## Principais insights
* Os metadados textuais do acervo demonstraram conter informações relevantes para apoiar a sugestão automática de descritores em processos de catalogação e indexação.
* A maior parte dos erros ocorreu entre categorias semanticamente próximas, indicando que os modelos frequentemente identificam o contexto geral das obras, ainda que nem sempre prevejam o descritor principal registrado.
* Modelos clássicos de classificação textual baseados em TF-IDF apresentaram resultados consistentes em uma base com mais de 155 mil registros distribuídos em 100 categorias temáticas.
* A exploração complementar com Word2Vec revelou relações semânticas coerentes entre termos do acervo, evidenciando potencial para enriquecimento de metadados e apoio à construção e revisão de vocabulários controlados.
* Os resultados reforçam o potencial de técnicas de Machine Learning e Processamento de Linguagem Natural como ferramentas de apoio à catalogação, indexação e recuperação da informação, sempre em complemento à análise especializada realizada pelos profissionais responsáveis pelos acervos.

## Desempenho dos modelos
| Modelo              | Acurácia (Teste) | Validação Cruzada |
| ------------------- | ---------------: | ----------------: |
| Naive Bayes         |            44,0% |             43,1% |
| Logistic Regression |            52,8% |             51,9% |
| LinearSVC           |        **53,8%** |         **53,3%** |

**Modelo selecionado:** LinearSVC  
**Exploração complementar:** Word2Vec (vocabulário com 4.746 termos)

## Aplicações em acervos culturais
* Sugestão automática de descritores
* Apoio à catalogação e indexação
* Revisão e enriquecimento de metadados
* Apoio à construção e revisão de vocabulários controlados
* Recuperação da informação

## Como executar
1. Abra o notebook pelo botão **Open in Colab** disponível no topo deste repositório.
2. Execute todas as células do início ao fim. O tempo aproximado de execução completa é de 20 minutos.
3. O notebook foi desenvolvido para execução em Google Colab e utiliza o dataset público do **Metropolitan Museum of Art (Met)** carregado diretamente por URL. Informações adicionais sobre a base de dados estão disponíveis na pasta [`data/`](data/).
4. Acompanhe a narrativa do notebook, incluindo as etapas de análise exploratória (EDA), modelagem, avaliação dos modelos e exploração semântica com Word2Vec.
   
## Autora
Charlyne Scaldini  
Historiadora | Estruturação da informação e qualidade de dados para acervos digitais  
[LinkedIn](https://www.linkedin.com/in/charlyne-scaldini-92959a2b2)  
chascaldini@gmail.com

