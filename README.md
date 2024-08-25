# Implementação de NLU com Rede Neural
Feito por Raphael Lisboa, Mateus Almeida, Thomas Barton e Vitor Barros

Nesta atividade foi desenvolvida uma rede neural, com uma camada de Embedding e utilizando LSTM, para classificações de intenções das frases da base de dados do projeto. Além disso, uma abordagem de Word2Vec pré-treinado com cbow50 também foi feita. Os resultados foram passados para o Tensorboard para visualização

## Resultados
### Rede Neural
![Métricas da rede neural](https://github.com/user-attachments/assets/43a65ce6-87c3-4f18-b50b-1224bb2b550b)

Pelas métricas é possível perceber que o modelo obteve 45% de acurácia. As outras métricas mostraram que nem todas as classes estavam no dataset de teste, já que algumas tiveram 0 como resultado, ou seja, provavelmente não havia nenhuma ocorrência para ser predita.


![Exemplo no tensorboard](https://github.com/user-attachments/assets/84a1996e-717c-43a8-b762-bb2dc69e2fcd)

O tensorboard resume informações do modelo durante o treinamento. Na imagem é possível ver uma de várias métricas armazenadas, a acurácia por época. É possível perceber que a acurácia de treino aumentou gradualmente ao longo das épocas, mas a de validação apresentou uma variação maior, mas dentro de um intervalo. Isto mostra sinais de um possível overfitting ao obter altas acurácias no treinamento e baixas na validação.

### Word2Vec
![Métricas word2vec](https://github.com/user-attachments/assets/44bc6d71-f584-4c3d-9af0-d74f3e3c426b)

O Word2Vec apresentou uma acurácia superior a rede neural, 75%. No entanto, também apresentou classes que não estavam presentes no conjunto de teste.

![Embedding Projector](https://github.com/user-attachments/assets/9a64b73e-2a15-45ee-89d2-9f0df553ffbb)

Aqui temos as frases da base de dados em uma projeção de acordo com seus valores do Word2Vec. Com ele é possível analisar frases que são próximas, e assim, apresentam uma maior similaridade.

No google colab(https://colab.research.google.com/drive/1WXqfdLlvxXZXp41e-9Va5xNdUpX2wthR?usp=sharing) é possível visualizar o tensorboard e o embedding projector (necessário desativar a opção de visualização 3D - quadrado com A no menu superior) - no notebook .ipynb não ficou salvo.
