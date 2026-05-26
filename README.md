# Sentinela Fire ACV

Projeto da Global Solution 2026 para a disciplina **Applied Computer Vision**.

A proposta e desenvolver uma solucao de visao computacional para monitoramento, classificacao e previsao de risco de queimadas. O notebook treina redes neurais convolucionais criadas do zero para classificar imagens em tres classes operacionais:

- Vegetacao umida: baixo risco
- Vegetacao seca: risco moderado
- Foco de queimada: alto risco

O modelo usa as imagens `umida.jpg`, `seca.jpg` e `queimada.jpg` como base do dataset. A partir delas, o notebook gera recortes aumentados com variacoes de brilho, contraste, rotacao, espelhamento e ruido. A classificacao visual e combinada com metadados climaticos e orbitais simulados para produzir um nivel de alerta operacional.

## Integrantes

- Deivison Pertel - RM 550803
- Eduardo Akira Murata - RM 98713
- Wesley Souza de Oliveira - RM 97874

## Arquivos do projeto

- `GS_Sentinela_ACV.ipynb`: notebook principal com geracao do dataset, treinamento, avaliacao e demonstracao funcional.
- `umida.jpg`: imagem-base da classe de baixo risco.
- `seca.jpg`: imagem-base da classe de risco moderado.
- `queimada.jpg`: imagem-base da classe de alto risco.

## Como executar no Google Colab

1. Abra o arquivo `GS_Sentinela_ACV.ipynb` no Google Colab.
2. No menu lateral esquerdo, abra a aba **Arquivos**.
3. Faca upload dos arquivos `umida.jpg`, `seca.jpg` e `queimada.jpg` para a raiz do ambiente, no mesmo nivel da pasta `sample_data`.
4. Confirme que os arquivos foram enviados executando:

```python
!ls -lh umida.jpg seca.jpg queimada.jpg
```

5. No menu superior, selecione **Ambiente de execucao > Reiniciar e executar tudo**.

Observacao: arquivos enviados manualmente ao Colab ficam disponiveis apenas durante a sessao atual. Se o ambiente for reiniciado, sera necessario fazer upload das imagens novamente.

## Como executar localmente

1. Mantenha os quatro arquivos na mesma pasta:

```text
GS_Sentinela_ACV.ipynb
umida.jpg
seca.jpg
queimada.jpg
```

2. Abra o notebook no Jupyter, VS Code ou ambiente compativel.
3. Execute a primeira celula para instalar as dependencias.
4. Reinicie o kernel se o ambiente solicitar.
5. Execute todas as celulas do notebook.

## Dependencias principais

O notebook instala e utiliza:

- TensorFlow/Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Pillow

## Resultado esperado

Ao final da execucao, o notebook apresenta:

- amostras geradas a partir das imagens-base;
- divisao entre treino, validacao e teste;
- duas arquiteturas de CNN treinadas do zero;
- comparacao entre modelos;
- matriz de confusao;
- analise de acertos e erros;
- demonstracao funcional com alerta de risco para novas cenas.
