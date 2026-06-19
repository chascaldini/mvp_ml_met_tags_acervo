# Classificação textual e técnicas de NLP para apoio à catalogação e sugestão de descritores em acervos culturais: um estudo com o Met Open Access
MVP de Machine Learning aplicado a acervos culturais | Pós-Graduação em Data Science & Analytics | PUC-Rio

### Acesse o projeto completo:
[![Open in Colab](https://img.shields.io/badge/Open%20in-Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com/drive/1VWpG1qHCgHeC20rcwfWGXnnmi8cpWWcb?usp=sharing)

## O desafio
Descritores são elementos fundamentais para a organização, recuperação e descoberta de informações em acervos culturais. Mas será que é possível identificar padrões nos próprios metadados das obras e utilizá-los para apoiar a sugestão automática desses descritores?

Este projeto explora essa questão por meio de técnicas de Machine Learning e Processamento de Linguagem Natural (NLP), utilizando o dataset Open Access do Metropolitan Museum of Art (The Met). A proposta é investigar até que ponto informações presentes em campos como título, material, tipologia e contexto institucional podem contribuir para processos de catalogação e indexação assistidos por inteligência artificial.

> É possível aprender padrões relevantes nos metadados de um acervo e utilizá-los para sugerir descritores de forma automatizada?

## Fluxo do projeto
Definição do problema → Carga dos dados → Inspeção inicial → EDA → Seleção de variáveis → Pré-processamento → Modelagem → Avaliação → Otimização → Exploração semântica → Interpretação dos resultados

## Abordagem metodológica
EDA • NLP • TF-IDF • Classificação supervisionada • Validação cruzada • Otimização de hiperparâmetros • Exploração semântica com Word2Vec  
**Modelos avaliados:** Multinomial Naive Bayes (baseline), Logistic Regression e LinearSVC.  
**Tecnologias:** Python, Pandas, Scikit-Learn, Plotly, Gensim e Google Colab.  

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

## Boas práticas e reprodutibilidade

### Ambiente de execução
- Google Colab
- Seed fixa: `42`
- Dataset carregado diretamente do repositório Open Access do [Metropolitan Museum of Art (Met)](data/)
- Tempo aproximado de execução completa: 20 minutos

1. Para explorar todas as etapas do projeto, utilize o botão **Open in Colab** disponível no topo deste repositório.
3. Executar todas as células do início ao fim
4. Acompanhar a narrativa do notebook, incluindo EDA, modelagem, avaliação dos modelos e exploração semântica com Word2Vec.

### Definição do problema
* Coluna original: `Tags`
* Variável alvo criada: `Tag_principal`
* Restrição às 100 Tags mais frequentes do dataset

### Features utilizadas
* `Title`
* `Medium`
* `Object Name`
* `Classification`
* `Department`

### Estratégia de avaliação
* Holdout 80/20 estratificado
* Validação cruzada
* Classification Report
* Matriz de Confusão
* Análise qualitativa das previsões

### Otimização
* Ajuste manual do hiperparâmetro `C` do LinearSVC
* Valores testados: `0.5`, `1.0` e `2.0`
* Melhor configuração identificada: `C = 1.0`

### Limitações
* Simplificação do problema multilabel por meio da variável `Tag_principal`
* Restrição às 100 Tags mais frequentes
* Utilização exclusiva de metadados textuais, sem análise das imagens das obras
* Representação textual baseada principalmente em TF-IDF

## Autora
Charlyne Scaldini  
[LinkedIn](https://www.linkedin.com/in/charlyne-scaldini-92959a2b2)  
chascaldini@gmail.com

