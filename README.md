# Transfer Learning – Binary Classification (Colab)

Este repositório contém um **notebook pronto** para você treinar uma rede neural com **Transfer Learning** no **Google Colab** usando `TensorFlow/Keras`. Não precisa saber Python: basta abrir o notebook, seguir as instruções em cada célula e executar (botão ▶️).

## Objetivo
Aplicar Transfer Learning em um problema de **duas classes** (por exemplo, `cats_vs_dogs`), documentar o processo e publicar no GitHub.

## Como usar (passo a passo)
1. Abra o Google Colab: https://colab.research.google.com/
2. Faça upload do arquivo `transfer_learning_colab.ipynb` para o Colab (ou suba no seu Google Drive e abra por lá).
3. Siga as células do notebook de cima para baixo, clicando em ▶️ para executar.
4. Por padrão, o notebook usa o **dataset `cats_vs_dogs`** através do `tensorflow_datasets (tfds)`. 
5. Se quiser usar seu **dataset próprio**, troque a variável `USE_TFDS = False` e aponte a pasta no Google Drive com a estrutura:
   ```
   dataset/
     class_a/
       img001.jpg
       img002.jpg
     class_b/
       img010.jpg
       img011.jpg
   ```

## O que este notebook faz
- Carrega dados via **TFDS** (`cats_vs_dogs`) **OU** do seu Google Drive (pasta com duas classes).
- Pré-processa imagens (redimensionamento, normalização e aumentos simples de dados).
- Carrega **MobileNetV2** pré-treinada no ImageNet (camadas congeladas).
- Adiciona camadas finais para **2 classes** (saída sigmoide).
- Treina por poucas épocas (você pode aumentar).
- Avalia no conjunto de validação/teste.
- Salva o modelo treinado (`.keras`).
- (Opcional) Gera gráfico simples de acurácia e perda.

## Estrutura 
```
transfer-learning-binary/
├── transfer_learning_colab.ipynb
├── README.md
└── images/                # (opcional) coloque screenshots aqui
```

## Entrega (DIO)
- Repositório público no GitHub com:
  - `README.md` (este arquivo)
  - `transfer_learning_colab.ipynb`
  - Pasta `images/` 


## Requisitos
- Google Colab (recomendado)
- TensorFlow 2.x (já vem no Colab)
- `tensorflow_datasets` (já vem no Colab)

## Dicas
- Comece com poucas épocas (ex.: `epochs=3`). Se rodar rápido, aumente.
- Se usar dataset próprio, garanta **equilíbrio** (número parecido de imagens por classe).
- Documente o que você fez: parâmetros, resultados, observações.

---

### Autor
Este material foi preparado para execução simples por **Tiago Aguioncio Vieira (ZENNE)**.
