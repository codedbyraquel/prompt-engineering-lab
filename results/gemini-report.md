
# Relatório Experimental — Gemini

## 1. Objetivo

Avaliar o desempenho das técnicas Zero-shot e Few-shot
Prompting na classificação automatizada de sentimentos
em avaliações complexas de restaurantes.

## 2. Ambiente experimental

- Linguagem: Python.
- Ambiente de desenvolvimento: Google Colab.
- Modelo: Gemini 3.1 Flash-Lite.
- Integração: Google Gemini API.
- Bibliotecas: Pandas, Requests e Google GenAI.
- Data: 25/11/2026.

## 3. Dataset

O conjunto de dados é composto por 20 avaliações fictícias,
distribuídas igualmente entre quatro categorias:

- Positivo: 5.
- Negativo: 5.
- Neutro: 5.
- Misto: 5.

As avaliações apresentam desafios linguísticos como
sarcasmo, ironia, negação, contradições, linguagem informal
e erros ortográficos.

## 4. Metodologia

Os prompts foram carregados automaticamente do GitHub
e preenchidos dinamicamente com as avaliações do dataset.

As classificações foram realizadas por meio da API do
Gemini e comparadas com os sentimentos esperados.

Foram realizadas 40 classificações no experimento principal,
sendo 20 para cada técnica.

## 5. Resultados

| Métrica | Zero-shot | Few-shot |
|---|---:|---:|
| Avaliações | 20 | 20 |
| Acertos originais | 19 | 18 |
| Erros originais | 1 | 2 |
| Acurácia original | 95% | 90% |
| Acertos após normalização | 19 | 19 |
| Acurácia normalizada | 95% | 95% |

## 6. Análise de erros

### Avaliação 11 — Sarcasmo

Texto: "Parabéns pela entrega! Só demorou duas horas."

- Sentimento esperado: negativo.
- Zero-shot: misto.
- Few-shot: misto.

Ambas as técnicas apresentaram divergência em relação
à classificação esperada, indicando uma possível
dificuldade na interpretação do sarcasmo.

### Avaliação 26 — Formatação

Texto: "A apresentação estava impecável, mas o sabor
deixou a desejar."

- Sentimento esperado: misto.
- Few-shot: classificação: misto.

O modelo identificou o sentimento esperado, porém
acrescentou um prefixo não solicitado, provocando
uma divergência na comparação textual.

## 7. Normalização das respostas

Foi implementada uma função de pós-processamento
responsável pela remoção de espaços, conversão para
letras minúsculas e remoção do prefixo "classificação:".

A regra de remoção do prefixo foi definida após a análise
dos erros observados.

Os resultados originais foram preservados para garantir
a transparência e a rastreabilidade do experimento.

## 8. Limitações

- Dataset reduzido e fictício.
- Classificações esperadas definidas manualmente.
- Apenas um modelo utilizado neste experimento.
- Ausência de múltiplas execuções independentes.
- Consumo de tokens e latência não avaliados.
- Normalização ajustada após a observação dos resultados.

## 9. Conclusão

O Zero-shot apresentou acurácia original de 95%,
enquanto o Few-shot obteve 90%.

Após a normalização das respostas, ambas as técnicas
atingiram 95% de acurácia.

Os resultados demonstram a importância da engenharia
de prompts, da avaliação sistemática de modelos e do
pós-processamento das respostas em aplicações de IA.

Entretanto, a dimensão reduzida do dataset não permite
generalizar os resultados para outros contextos.

## 10. Próximas etapas

- Desenvolvimento de uma aplicação interativa.
- Validação das entradas e saídas do modelo.
- Implementação de respostas estruturadas.
- Publicação da aplicação na nuvem.
