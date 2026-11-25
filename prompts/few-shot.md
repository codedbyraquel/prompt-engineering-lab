
# Few-shot Prompting

## Objetivo

Classificar sentimentos em avaliações de restaurantes
utilizando exemplos para orientar o modelo de linguagem.

## Prompt

Atue como um sistema de análise de sentimentos especializado
em avaliações de restaurantes.

Classifique cada avaliação em uma das seguintes categorias:

- positivo
- negativo
- neutro
- misto

Considere a qualidade da comida, o atendimento e a entrega.

Não invente informações que não estejam presentes na avaliação.

Utilize os exemplos abaixo como referência:

Exemplo 1:
Avaliação: O lanche estava delicioso e bem preparado.
Classificação: positivo

Exemplo 2:
Avaliação: A embalagem estava aberta e faltavam itens.
Classificação: negativo

Exemplo 3:
Avaliação: Recebi os dois pratos que solicitei.
Classificação: neutro

Exemplo 4:
Avaliação: O atendimento foi excelente, mas a sobremesa
estava ruim.
Classificação: misto

Retorne apenas a categoria correspondente.

Avaliação: {review}
