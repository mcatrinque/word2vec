# Implementação Word2Vec

Esta implementação destina-se a treinar e avaliar modelos Word2Vec usando a biblioteca Gensim. Os modelos Skip-Gram e CBOW (Continuous Bag of Words) são explorados com diferentes conjuntos de parâmetros para capturar representações semânticas e sintáticas de palavras em um corpus.

## Descrição do Problema

A tarefa principal é treinar modelos Word2Vec capazes de aprender representações distribuídas de palavras em um corpus textual. A avaliação dos modelos inclui a precisão em analogias de palavras, a precisão por categoria e a visualização 2D usando t-SNE.

## Objetivos do Trabalho

1. **Treinamento de Modelos Word2Vec:**
   - Treinar modelos Skip-Gram e CBOW com diferentes configurações de hiperparâmetros.

2. **Avaliação dos Modelos:**
   - Avaliar modelos em analogias de palavras.
   - Calcular a precisão por categoria.
   - Visualizar a distribuição 2D de palavras usando t-SNE.

3. **Visualização dos Melhores Resultados:**
   - Exibir os melhores resultados em cada métrica para análise detalhada.

## Descrição das Funções

### `train_word2vec_model`

```python
def train_word2vec_model(corpus_path, vector_dim, context_window_size, downsampling_threshold, num_threads, output_format, epochs, hs, negative, min_count):
    # ... (ver código completo para detalhes)
    return model
```

Esta função treina um modelo Word2Vec com base nos parâmetros fornecidos e salva o modelo treinado.

### `evaluate_word2vec_model`

```python
def evaluate_word2vec_model(model, analogy_file, model_name, params):
    # ... (ver código completo para detalhes)
    return evaluation_results
```

Esta função avalia um modelo Word2Vec em termos de acurácia em analogias de palavras, precisão por categoria e similaridade de cosseno entre pares de palavras.

### `display_best_results`

```python
def display_best_results(results_list, model_names, param_sets):
    # ... (ver código completo para detalhes)
    plt.show()
```

Esta função exibe os melhores resultados dos modelos em diferentes métricas em tabelas e gráficos.

## Modelos e Parâmetros

Dois tipos de modelos são treinados: Skip-Gram e CBOW. Os seguintes parâmetros são variados durante o treinamento:

- `vector_dim`: Dimensão do vetor de palavra.
- `context_window_size`: Tamanho da janela de contexto.
- `downsampling_threshold`: Limiar de downsampling.
- `num_threads`: Número de threads para treinamento.
- `output_format`: Formato de saída do modelo.
- `epochs`: Número de épocas de treinamento.
- `hs`: Hierarchical Softmax (0 para negativo sampling, 1 para Hierarchical Softmax).
- `negative`: Número de amostras negativas para treinamento.
- `min_count`: Contagem mínima de palavras para considerar no vocabulário.

## Execução do Código

Para treinar e avaliar os modelos, execute o código fornecido nas células do Jupyter Notebook. Certifique-se de ter o ambiente configurado com as bibliotecas necessárias.

**Importante:** O tempo de execução pode variar com base nos parâmetros e no tamanho do corpus.

## Resultados

Os resultados incluem métricas de avaliação, visualizações 2D e gráficos de precisão. Os melhores resultados são destacados para análise aprofundada.
