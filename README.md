# Análise Preditiva de Notas de Estudantes: Regressão Linear vs KNN

Este repositório contém o código-fonte e o artigo final do projeto "Análise Preditiva de Notas de Estudantes Baseada em uma Comparação entre os Algoritmos Regressão Linear e K-Nearest Neighbors", desenvolvido por alunos do curso de Ciência da Computação do Centro Universitário de Maceió (UNIMA).

## 📄 Sobre o Projeto

O avanço das tecnologias e a popularização dos jogos eletrônicos têm transformado os hábitos dos jovens, levantando questões sobre o impacto dessas atividades no desempenho acadêmico. Este trabalho tem como objetivo realizar uma análise preditiva das notas escolares de estudantes com idades entre 16 e 25 anos.

Para isso, realizou-se um estudo comparativo empírico entre dois algoritmos de Machine Learning (Mineração de Dados Educacionais):
- **Regressão Linear Múltipla** (Modelo paramétrico)
- **K-Nearest Neighbors (KNN) Regressor** (Modelo não-paramétrico)

Os resultados do estudo demonstraram que a Regressão Linear Múltipla obteve um desempenho superior ($R^2 \approx 0,91$), sugerindo que a relação entre os hábitos de vida estudados (sono, horas de estudo, tempo de jogo) e o rendimento escolar possui uma forte tendência linear. O trabalho também conclui que o tempo dedicado aos jogos não afeta negativamente as notas de forma isolada, desde que mantido um "limiar de equilíbrio" aliado a uma boa higiene do sono (7 a 8 horas) e alta presença escolar (superior a 85%).

## 📁 Estrutura do Repositório

- `Artigo_Regressão_Linear_vs_KNN.ipynb`: Notebook Jupyter contendo todo o código utilizado na pesquisa. Inclui as etapas de:
  - Pré-processamento e Análise Exploratória dos Dados.
  - Padronização matemática das variáveis (*Z-score standardization* via `StandardScaler`).
  - Treinamento do modelo de Regressão Linear Múltipla.
  - Treinamento e ajuste fino do KNN Regressor (busca do número ótimo de vizinhos $K$ utilizando `GridSearchCV` e validação cruzada `RepeatedKFold`).
  - Avaliação de métricas de erro ($R^2$, MAE, MSE, RMSE).
  - Plotagem dos gráficos comparativos de desempenho.
- `Artigo_IA_Versao_Final.pdf` (ou similar): Arquivo em formato PDF contendo a versão final do manuscrito acadêmico submetido, formatado nos padrões IEEE. Inclui toda a fundamentação teórica, referencial bibliográfico e as minúcias metodológicas.

## 📊 Conjunto de Dados (Dataset)

Os dados modelados provêm do dataset público **Gaming vs Academic Performance** disponível na plataforma Kaggle. Ele consolida 1000 amostras com registros de comportamento digital, contendo variáveis contínuas e categóricas como:
- Horas diárias de jogos (`gaming_hours`) e estudos (`study_hours`)
- Qualidade e horas de sono (`sleep_hours`)
- Taxa de frequência escolar (`attendance`)
- Idade, tempo de tela, tempo de reação, etc.

A variável alvo (Target) da predição foram as notas reais finais alcançadas pelos estudantes (`grades`), em escala de 0 a 100.

## 🛠️ Tecnologias e Bibliotecas Utilizadas

O experimento de Machine Learning foi conduzido na linguagem de programação **Python 3**, processado no ambiente computacional em nuvem do **Google Colab**. O ecossistema de software engloba as bibliotecas:
- **Pandas e NumPy:** Para estruturação, limpeza e cálculos matriciais.
- **Scikit-Learn:** Framework principal para as tarefas de regressão (`LinearRegression`, `KNeighborsRegressor`), padronização e validação.
- **Matplotlib e Seaborn:** Para a construção e estilização de visualizações de dados, inferências visuais de correlação e dispersão de erros.

## 🚀 Como Executar Localmente

1. Clone este repositório em seu ambiente local:
   ```bash
   git clone https://github.com/BrunoSantos751/Artigo_Regress-o_Linear_vs_KNN.git
   ```
2. Pela natureza computacional, recomenda-se fortemente o uso do **Google Colab** para executar o notebook. Basta fazer o upload do arquivo `.ipynb`.
3. Caso deseje executar localmente via Jupyter Notebook ou Jupyter Lab, assegure-se de ter um ambiente Python configurado com os pacotes descritos acima (`pip install pandas numpy scikit-learn matplotlib seaborn`).
4. Execute as células em ordem sequencial. *Nota: certifique-se de referenciar corretamente o caminho do dataset (arquivo .csv) no ato da leitura do Pandas caso o baixe do Kaggle.*

## 👥 Autores e Pesquisadores

- Bruno Santos Moraes
- Fabio Fernandes Reis Filho
- João Honório Barbosa
- Maria Layanne Rodrigues da Silva
- Mateus dos Santos Ferreira
- Vinícius Matheus da Silva

**Instituição:** Centro Universitário de Maceió (UNIMA)  
**Curso:** Ciência da Computação
