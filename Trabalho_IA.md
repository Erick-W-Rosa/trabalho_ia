📘 RELATÓRIO – Comparação de Modelos de Machine Learning (SVM, Random Forest, KNN)

Dataset: Iris Dataset – scikit-learn

Aluno: Erick William da Rosa

🧩 1. Introdução

O objetivo deste trabalho é comparar o desempenho de três algoritmos clássicos de Machine Learning supervisionado aplicados ao dataset Iris:

- SVM (Support Vector Machine)

- Random Forest

- KNN (K-Nearest Neighbors)

Todos os modelos foram implementados utilizando Python e as bibliotecas:

- pandas

- matplotlib

- scikit-learn

O conjunto de dados Iris é composto por 150 amostras de flores, divididas igualmente em três classes:

- Setosa

- Versicolor

- Virginica

Cada amostra possui quatro características numéricas:

- Comprimento da sépala

- Largura da sépala

- Comprimento da pétala

- Largura da pétala

Os dados foram divididos em:

- 70% para treino

- 30% para teste

- Em divisão estratificada (mantendo a proporção das classes)

🧪 2. Resultados Obtidos

A seguir estão os resultados extraídos diretamente das execuções dos três modelos.

🔵 2.1 SVM (Support Vector Machine)
Acurácia: 0.9556 (95,56%)
Matriz de Confusão

- Acertou todas as instâncias da classe Setosa

- Errou 1 amostra de Versicolor, classificando como Virginica

Resumo

- Ótimo desempenho geral

- Forte separação entre classes

- Poucos erros em classes similares (Versicolor x Virginica)

🌲 2.2 Random Forest
Acurácia: 0.8889 (88,89%)
Matriz de Confusão

- Acertou todas as Setosa

- Teve mais erros entre Versicolor e Virginica, comum em modelos baseados em árvores por causa da variação dos splits

Resumo

- Modelo rápido de treinar

- Erros maiores em classes com fronteiras suaves

- Desempenho geral inferior ao SVM e KNN neste dataset

🟢 2.3 KNN (K-Nearest Neighbors)
Acurácia: 0.9778 (97,78%)
Matriz de Confusão

- Acertou praticamente todas as amostras

- Apenas 1 erro entre Versicolor e Virginica

Resumo

- Melhor desempenho entre todos os modelos

- K=5 funcionou muito bem para este dataset

- Simples, porém altamente eficaz quando os dados estão limpos e bem distribuídos

📊 3. Comparação Direta Entre os Modelos
Modelo	Acurácia	Erros Principais
KNN	97,78%	1 erro entre classes vizinhas
SVM	95,56%	1 erro Versicolor/Virginica
Random Forest	88,89%	4 erros Virginica → Versicolor
📌 Interpretação:

- KNN foi o melhor modelo no conjunto Iris.
    - O dataset é pequeno e bem separado → favorece classificadores baseados em distância.

- SVM teve desempenho excelente, ficando muito próximo do KNN.

- Random Forest teve o pior desempenho, porém ainda acima de 88%.
    - Árvores podem ter dificuldades em datasets com fronteiras muito suaves.

🧠 4. Conclusões

Com base nos experimentos realizados:

- O KNN mostrou-se o algoritmo mais preciso neste dataset, beneficiado pela distribuição bem definida das classes.

- O SVM também apresentou excelente performance, sendo eficiente para fronteiras complexas.

- O Random Forest, apesar de bom, teve mais dificuldade em diferenciar as espécies Versicolor e Virginica.

📌 Considerações finais:

- Para bancos de dados pequenos e bem separados: KNN é extremamente eficiente.

- Para dados maiores e mais complexos: SVM costuma ter melhor escalabilidade.

- Random Forest é ótimo por padrão, mas não foi o ideal neste cenário específico.
