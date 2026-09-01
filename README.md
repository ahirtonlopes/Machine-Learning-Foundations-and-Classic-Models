# Machine Learning Foundations & Classic Models

Material aberto da disciplina **Machine Learning Foundations & Classic Models**, do MBA em AI Engineering & Multi Agents da FIAP.

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3+-orange?style=flat-square&logo=scikit-learn)
![Colab](https://img.shields.io/badge/Google-Colab-yellow?style=flat-square&logo=googlecolab)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

## Sobre

Os modelos mudam e as ferramentas evoluem, mas quem entende Machine Learning domina a base que sustenta toda a revolução da IA moderna. A disciplina cobre fundamentos e métricas de avaliação, modelos clássicos e séries temporais, reinforcement learning, redes neurais, backpropagation e casos práticos.

## Estrutura

```
Datasets/    bases usadas pelas demos
Notebooks/   demos práticas, prontas para rodar no Google Colab
Slides/      decks das aulas
```

> O deck publicado aqui omite figuras de terceiros sujeitas a restrição de redistribuição, então a numeração pode diferir em um ou outro slide da versão apresentada em aula.

## Demos

| Demo | Tema | Conceitos |
|---|---|---|
| [Demo 1](Notebooks/Demo1_URL_Classifier.ipynb) | Classificação de URL potencialmente maliciosa | Aprendizado supervisionado, TF-IDF, regressão logística, holdout, acurácia, baseline |
| [Demo 2](Notebooks/Demo2_Fraud_Detection.ipynb) | Detecção de fraude em pagamentos | Vazamento de alvo, matriz de confusão, precisão, recall, F1, desbalanceamento, trade-off precisão/recall |
| [Demo 3](Notebooks/Demo3_Comparacao_Metricas.ipynb) | Comparação de métricas de regressão | Regressão linear, MAE, MSE, RMSE, MAPE, R², R² ajustado, validação cruzada com K-pastas |
| [Demo 3.5](Notebooks/Demo3_5_Time_Series_Call_Center_Forecast.ipynb) | Introdução a séries temporais (call center) | Tendência, sazonalidade, features temporais, divisão treino/teste respeitando o tempo, baseline |
| [Demo 4](Notebooks/Demo4_Fraud_Detection.ipynb) | Classificação de fraude em pagamentos | Aprendizagem supervisionada, regressão logística, árvore de decisão, acurácia, precisão, recall |
| [Demo 5](Notebooks/Demo5_Kmeans_Mall_Customers.ipynb) | Segmentação de clientes de shopping | Aprendizagem não supervisionada, K-Means, método do cotovelo, silhueta, personas de negócio |
| [Demo 6](Notebooks/Demo6_Kmeans_Crime_data.ipynb) | Mapa de crimes de Toronto | K-Means sobre coordenadas geográficas, agrupamento espacial, análise exploratória |
| [Demo 7](Notebooks/Demo7_Q_Learning_Taxi.ipynb) | Táxi do Gymnasium | Reinforcement learning, agente/ambiente/recompensa, Q-learning, Q-table |
| [Demo 8](Notebooks/Demo8_Q_Learning_FrozenLake.ipynb) | FrozenLake | Q-learning em ambiente estocástico, exploração vs. explotação |
| [Demo 9](Notebooks/Demo9_Bellman.ipynb) | Equação de Bellman | Valor de estado, recompensa descontada, plano ótimo em grade |

A Demo 2 merece um aviso: ela começa com um modelo que acerta 100% e usa esse resultado bom demais para ensinar a reconhecer **vazamento de alvo**, seguindo por que a acurácia engana em base desbalanceada e como precisão e recall se contrapõem.

## Como rodar

Cada notebook abre direto no Google Colab. A primeira célula de código baixa a base necessária deste repositório com `curl`. Se preferir, há sempre uma célula logo abaixo com a alternativa de subir o arquivo do seu próprio computador: basta descomentar e executar.

Para rodar localmente:

```bash
pip install pandas numpy scikit-learn matplotlib
jupyter notebook
```

## Datasets

| Arquivo | Origem | Uso |
|---|---|---|
| `url_data.csv` | [Kaggle](https://www.kaggle.com/antonyj453/urldataset) | Demo 1 |
| `payment_fraud.csv` | [Kaggle](https://www.kaggle.com/pwnpen/payment) | Demos 2 e 4 |
| `Mall_Customers.csv` | [Kaggle](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python) | Demo 5 |
| `MCI_2014_to_2017.csv` | [Toronto Police Service](https://data.torontopolice.on.ca/search?tags=MCI) | Demo 6 |

A Demo 3 usa o dataset `diabetes`, que já vem com o scikit-learn, e a Demo 3.5 gera a própria série temporal simulada; nenhuma das duas precisa de download. As Demos 7 e 8 usam os ambientes `Taxi` e `FrozenLake` da biblioteca [Gymnasium](https://gymnasium.farama.org/); a Demo 9 gera sua própria grade; nenhuma delas precisa de dataset externo. [`Grid_movements_RL.ipynb`](Notebooks/Grid_movements_RL.ipynb) é material de apoio para entender os movimentos em grade usados na Demo 9.

## Autor

**Prof. Dr. Ahirton Lopes** · Data & AI Senior Manager na Accenture · Professor de MBA e Corporate na FIAP e Alura · 3x Google Developer Expert

[LinkedIn](https://www.linkedin.com/in/ahirtonlopes) · [GitHub](https://github.com/ahirtonlopes) · profahirton.lopes@fiap.com.br

## Licença

MIT. Veja [LICENSE.md](LICENSE.md).
