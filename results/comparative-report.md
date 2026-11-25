
# Análise Comparativa — Zero-shot vs Few-shot

## Objetivo

Comparar o desempenho das técnicas Zero-shot e Few-shot
Prompting na classificação de sentimentos em avaliações
de restaurantes.

## Metodologia

- Ferramenta: ChatGPT.
- Versão exata do modelo: não registrada.
- Data: 25/11/2026.
- Base de dados: 10 avaliações fictícias.
- Total de classificações: 20.
- Execução: manual.
- Métrica: acurácia.
- Categorias: positivo, negativo, neutro e misto.

## Resultados

| Métrica | Zero-shot | Few-shot |
|---|---:|---:|
| Exemplos no prompt | 0 | 4 |
| Avaliações | 10 | 10 |
| Acertos | 10 | 10 |
| Erros | 0 | 0 |
| Acurácia | 100% | 100% |

## Análise dos resultados

As duas técnicas apresentaram desempenho equivalente
na classificação das avaliações iniciais.

A inclusão de exemplos no Few-shot Prompting não
proporcionou aumento da acurácia nesta base de dados.

O Zero-shot apresentou uma estrutura de instrução
mais curta, indicando potencial para menor consumo
de tokens de entrada.

## Limitações

- Quantidade reduzida de avaliações.
- Utilização de dados fictícios.
- Ausência de comentários suficientemente complexos.
- Execução manual dos testes.
- Versão exata do modelo não registrada.
- Consumo de tokens e latência não mensurados.

Os resultados não permitem concluir que as duas
técnicas apresentam desempenho equivalente em
cenários reais ou em bases de dados maiores.

## Próximas etapas

- Construir uma base de dados mais complexa.
- Avaliar sarcasmo, ironia e ambiguidades.
- Comparar novamente as técnicas.
- Implementar respostas estruturadas em JSON.
- Automatizar experimentos com Python.
- Avaliar novas métricas de desempenho.
