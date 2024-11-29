# Relatório Técnico: Implementação e Análise do Algoritmo de K-Means

## Autores
- Álisson Natan dos Anjos Pinheiro
- Larissa Ribeiro Firminio

**Data**: 29/11/2024

---

## Resumo
Este projeto teve como objetivo aplicar o algoritmo de **K-means** para a análise de agrupamento de dados do dataset *Human Activity Recognition using Smartphones*. As etapas principais envolveram:

1. **Análise exploratória dos dados**
2. **Implementação do modelo de K-means**
3. **Normalização e Repetição do Modelo**
4. **Avaliação da qualidade dos clusters**

O número ideal de clusters foi determinado utilizando métodos como o **Elbow Method** e o **Silhouette Score**. O modelo foi otimizado com a normalização dos dados e a inicialização **K-means++**, resultando em uma boa separação dos clusters, com inércia reduzida e um Silhouette Score satisfatório.

---

## Introdução
A área de reconhecimento de atividades humanas com dados coletados por smartphones tem grande aplicabilidade em saúde e automação. Este projeto utilizou o dataset *Human Activity Recognition using Smartphones*, que contém dados de sensores (acelerômetro e giroscópio) de 30 voluntários realizando atividades diárias.

O objetivo foi aplicar o **K-means** para identificar padrões relacionados às diferentes atividades humanas. A escolha do algoritmo deve-se à sua simplicidade e eficiência em tarefas de agrupamento sem supervisão.

---

## Metodologia
A metodologia foi dividida nas seguintes etapas:

### 1. Análise Exploratória dos Dados
Incluiu:
- **Distribuição das variáveis**: Gráficos de boxplot e histogramas.
- **Correlação entre variáveis**: Análise de matriz de correlação para identificar variáveis relevantes.
- **Redução de dimensionalidade**: Uso do *Principal Component Analysis* (PCA) para facilitar a visualização dos clusters.

### 2. Implementação do Algoritmo de K-means
- Uso do **K-means++** para inicialização eficiente dos centróides.
- Determinação do número ideal de clusters com os métodos:
  - **Elbow Method**
  - **Silhouette Score**

### 3. Normalização e Repetição do Modelo
- **Normalização**: Utilização do *StandardScaler* para reduzir a variabilidade nas escalas dos sensores.
- **Repetição**: Execução múltipla do modelo para verificar a consistência e confiabilidade dos clusters.

### 4. Avaliação e Métricas
- **Inércia**: Soma das distâncias quadradas entre os pontos e seus centróides.
- **Silhouette Score**: Avaliação da coesão e separação dos clusters.

**Resultados obtidos:**
- Inércia: **881007.9475**
- Silhouette Score: **0.4842**

Essas métricas indicaram:
- Boa coesão interna dos clusters.
- Boa separação entre os clusters.

A visualização dos clusters foi facilitada pelo uso do PCA, com gráficos 2D e 3D mostrando claramente a distribuição dos dados.

---

## Discussão
Embora os resultados tenham sido satisfatórios, algumas limitações foram observadas:
- **Escolha do número de clusters**: Definir o número ideal de clusters pode ser desafiador.
- **Qualidade dos dados**: Outliers e valores faltantes podem impactar os resultados.

A simplicidade e eficiência do **K-means** justificam sua escolha. No entanto, algoritmos como **DBSCAN** ou **Hierarchical Clustering** poderiam ser explorados em cenários mais complexos.

---

## Conclusão e Trabalhos Futuros
O projeto demonstrou a eficácia do **K-means** no agrupamento de dados de reconhecimento de atividades humanas. As etapas de análise exploratória, escolha do número de clusters e avaliação garantiram a qualidade dos resultados.

### Propostas de trabalhos futuros:
- Experimentação com outros algoritmos de clustering, como **Hierarchical Clustering** e **DBSCAN**.
- Inclusão de variáveis adicionais, como informações temporais e contextuais, para melhorar a precisão da classificação das atividades.

---

## Referências
- UCI Machine Learning Repository - Human Activity Recognition Using Smartphones Dataset.  
  [https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones](https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)
- Scikit-learn Documentation.  
  [https://scikit-learn.org/stable/documentation.html](https://scikit-learn.org/stable/documentation.html)
