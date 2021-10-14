# Machine_Learning_e_Redes_Neurais_LSTM_para_Previsão_do_Dólar

#### Aluno: André Bittencourt Pereira
#### Orientadora: [Manoela Kohler](https://github.com/manoelakohler)

---

Trabalho apresentado ao curso BI MASTER como pré-requisito para conclusão de curso e obtenção de crédito na disciplina [Projetos de Sistemas Inteligentes de
Apoio à Decisão](https://ica.puc-rio.ai/es/bi-master-es/).

---

### Resumo

O Dólar ocupa a posição de principal moeda de troca mundial, sendo utilizada no comércio internacional, nas reservas monetárias dos países e influenciando
diariamente a economia. A volatilidade de sua cotação, principalmente em relação ao Real, e a dificuldade de se prever o valor futuro justificam a tarefa de se testar
algumas técnicas em ciência de dados. Neste trabalho, foram testados alguns modelos de Marchine Learning e Redes Neurais LSTM considerando os dados de
Janeiro/2018 até Junho/2021 e obtidos bons resultados nos modelos preditivos, mesmo em um cenário que envolveu mudanças no cenário político com as eleições
de 2018 e a crise iniciada com o o COVID em 2020.

### 1. Introdução

Desde o Acordo de Bretton-Woods em 1944 e após o fim da 2a Guerra Mundial em 1945, com as nações européias muito fragilizadas economicamente pelos efeitos
do conflito, o Dólar passou a ocupar a posição de principal moeda de troca mundial, sendo utilizada pelos países como moeda de reserva e pelas empresas e
pessoas para transações internacionais.
O Dólar está no dia-a-dia das pessoas e empresas e a influência deste pode ser percebida na inflação, nos juros e no poder de compra em relação a todas as
moedas. Deste modo, é de fundamental importância tentar prever o comportamento do dólar, especialmente em relação ao Real que sofre grandes oscilações no
mercado de câmbio. O objetivo do trabalho será tentar prever o comportamento do Dólar em relação ao Real através de modelos de Machine Learning e utilizando as
Redes Neurais LSTM.

### 2. Modelagem

O trabalho foi elaborado utilizado os dados obtidos no Yahoo Finance (biblioteca python) no período de Janeiro/2018 até Junho/2021, montando 2 cenários básicos
de previsão: o 1o utilizando apenas a cotação do Dólar (Univariável) e o 2o usando dados de ativos e índices correlacionados com o Dólar tais como o índice
Ibovespa, a cotação do Petróleo, os juros do Tesouro Americano para 10 anos, VIX e DXY (Multivariável).
Foram testados os seguintes modelos de Machine Learning e Redes Neurais e comparados os resultados considerando como indicadores de acurácia o RMSE e o
R2:
Modelos Univariável: Prophet, ARIMA, XGBoost e Redes Neurais LSTM.
Modelos Multivariáveis: Regressão Linear Múltipla, Random Forest, XGBoost Regressor, SVM e Redes Neurais LSTM.

### 3. Resultados

Avaliando os resultados dos modelos univariável testados para a previsão do dólar, considerando apenas o preço do fechamento diário, foi observado que somente
as redes neurais LSTM tiveram bons resultados, tendo um RSME baixo de 0.012 e R2 alto de 0.99. Os modelos de Machine Learning Prophet, ARIMA e XGBoost
tiveram RMSE elevado e previsões muito distantes dos valores verificados para o dólar no período.
Observando os modelos multivariáveis, percebe-se um aumento considerável de eficácia através do maior R2 e menor RMSE do que nos modelos testados
considerando apenas o Dólar como variável. Modelos de Machine Learning como Random Forest e XGBoost Regressor tiveram R2 acima de 0.97 por exemplo. Isso
mostra como o mercado está correlacionado e ter um maior número de dados pode agregar aos modelos. A única exceção foi o LSTM que piorou os resultados
quando se colocou mais variáveis mas ainda teve bons resultados.

### 4. Conclusões

Os modelos de Machine Learning e as redes neurais foram eficientes na previsão do comportando do dólar principalmente com os modelos de Random Forest e
XGBoost utilizando múltiplas variáveis correlacionadas e as redes neurais LSTM que, mesmo só com os dados do Dólar, também teve bons resultados.
Uma possível evolução do trabalho no futuro seria a inclusão da análise de sentimento nos modelos preditivos, utilizando as redes sociais como mais uma fonte de
dados para monitorar o comportamento do Dólar em relação ao Real.

---

Matrícula: 192.110.156

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação Business Intelligence Master

