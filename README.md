# Análise de Dados Cinematográficos e Previsão de Nota IMDB

## 🎯 Objetivo

O objetivo é realizar uma análise em um banco de dados cinematográfico para orientar o estúdio sobre o tipo de filme a ser desenvolvido, com baseado em fatores que aumentam as chances de sucesso financeiro e aprovação na crítica do público. Foi construído um modelo de Machine Learning para prever a nota do IMDB de um filme com base em suas características.

## 🛠️ Ferramentas Utilizadas
* **Linguagem:** Python 3
* **Bibliotecas Principais:** Pandas, Matplotlib, Seaborn, Scikit-learn, WordCloud
* **Ambiente:** Google Colab

## 📂 Estrutura do Repositório
O projeto está organizado da seguinte forma:
- `PProductions.ipynb`: Notebook principal contendo toda a análise exploratória, pré-processamento e modelagem.
- `model.pkl`: Modelo de regressão (Random Forest) treinado e salvo, pronto para fazer previsões.
- `preprocessor.pkl`: Pipeline de pré-processamento treinado e salvo, usado para transformar novos dados.
- `requirements.txt`: Lista de dependências do Python para recriar o ambiente de execução.
- `README.md`: Este arquivo.

## 🚀 Como Executar o Projeto

1. **Clone o repositório (opcional):**
   ```bash
   git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
   ```
2. **Instale as dependências:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Execute o Notebook:**
   Abra o arquivo `.ipynb` em um ambiente Jupyter (como Jupyter Notebook, Jupyter Lab ou Google Colab) e execute as células em ordem.

## 📊 Análise e Metodologia

### Análise Exploratória de Dados (EDA)
A análise inicial revelou que os gêneros de **Ação** e **Aventura** são os que alcançam os maiores picos de faturamento e popularidade. Em contraste, **Drama** и **Biografia** são os gêneros com as maiores notas médias de crítica e público, porém com um teto de faturamento mais baixo.

### Pré-processamento
As etapas de preparação dos dados incluíram:
- Limpeza de nulos em `Gross` e `Meta_score`.
- Transformação da coluna `Genre` para `Primary_Genre` para simplificar a análise.
- Tratamento de alta cardinalidade para as colunas `Director` e `Star1`.

### Modelagem de Machine Learning
Para prever a nota do IMDB, foi desenvolvido um modelo de Regressão.
- **Modelo:** `RandomForestRegressor`.
- **Features Utilizadas:** Gênero, Diretor, Ator Principal, Ano de Lançamento, Duração, Faturamento, etc.
- **Performance:** O modelo bateu um Erro Médio Absoluto (MAE) de aproximadamente 0.15, indicando aproximadamente que as previsões de nota no IMDB erram por apenas 0.15 pontos.

## 📈 Resultados e Conclusão

Os principais fatores para um alto faturamento são o **gênero (Ação/Aventura)** e a **popularidade (alto número de votos)**. A nota do IMDB é um fator importante, mas não é garantia de sucesso financeiro.

A recomendação para a PProductions é o desenvolvimento de filmes de **Ação ou Aventura com uma narrativa forte**, capazes de atingir notas acima de 8.0, visando retorno financeiro melhor aprovação do público.
