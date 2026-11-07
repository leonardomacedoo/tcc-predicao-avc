# Predição de AVC sob desbalanceamento extremo de classes (PNS 2019)

Código do Trabalho de Conclusão de Curso **"Estudo comparativo de técnicas de aprendizagem de máquina para predição de AVC: uma análise sob desbalanceamento extremo de classes com microdados da PNS 2019"**, apresentado ao curso de Bacharelado em Sistemas de Informação do Instituto Federal Catarinense, Câmpus Araquari.

- **Autor:** Leonardo Macedo
- **Orientador:** Prof. Marcio Marcelo Piffer, Me.
- **Ano:** 2026

## Conteúdo

O notebook `tcc_predicao_avc.ipynb` reúne todas as etapas do trabalho, com as saídas da execução usada no texto:

1. leitura e tratamento dos microdados da Pesquisa Nacional de Saúde 2019;
2. análise exploratória;
3. divisão estratificada em treino e teste, com SMOTE aplicado apenas ao treino;
4. treinamento e avaliação de Regressão Logística, Random Forest, KNN e XGBoost;
5. experimentos complementares: sem balanceamento, ponderação de classes, curvas ROC e precisão-sensibilidade, ajuste do limiar de decisão, validação cruzada e razões de chance.

## Dados

Os microdados não estão neste repositório. O arquivo `pns2019.csv` (cerca de 920 MB) pode ser obtido no portal da PNS mantido pelo ICICT/Fiocruz:

<https://www.pns.icict.fiocruz.br/bases-de-dados/>

## Como executar

O notebook foi executado no Google Colab. Para reproduzir:

1. coloque o `pns2019.csv` na raiz do seu Google Drive (ou ajuste a variável `caminho_arquivo`);
2. abra o notebook no Colab e execute todas as células;
3. as tabelas e figuras são salvas na pasta indicada pela variável `PASTA` (`tcc_resultados_v5/`).

Todos os procedimentos aleatórios usam `random_state=42`. As versões das bibliotecas estão em `requirements.txt` e são impressas na última célula do notebook. Em outro sistema operacional, os resultados de Random Forest, KNN e XGBoost com SMOTE podem variar levemente.
