# Programa Brasil na Escola - Análise de Dados

## 📋 Sobre o Projeto

Análise exploratória e preditiva do dataset de escolas que aderiram ao Programa Brasil na Escola, investigando relações entre variáveis, identificando outliers e desenvolvendo modelos de regressão linear para previsão de verbas.

## 🎯 Objetivos

- **Identificar outliers** no dataset de escolas participantes do programa
- **Estudar correlações** entre as variáveis após limpeza dos dados
- **Desenvolver modelo preditivo** de regressão linear para previsão de verbas
- **Avaliar desempenho** dos modelos em casos atípicos (outliers)

## 📊 Fonte de Dados

**Base de escolas que aderiram ao Programa Brasil na Escola**
- Plataforma: [dados.gov.br](https://dados.gov.br/dados/conjuntos-dados/base-de-escolas-que-aderiram-ao-programa-brasil-na-escola)
- Período: Dados consolidados do programa
- Escopo: Nacional, por Unidades da Federação

## 🏫 Variáveis do Dataset

| Variável | Descrição | Tipo |
|----------|-----------|------|
| `UF` | Unidade da Federação | Categórica |
| `TOTAL_ESCOLA` | Quantidade de escolas participantes | Numérica |
| `MATRICULAS` | Número total de matrículas | Numérica |
| `VERBA` | Valor total da verba alocada (R$) | Numérica |

## 🔍 Principais Descobertas

### 📈 Correlações Identificadas
- **Forte correlação** entre `MATRICULAS` e `VERBA` (principal relação)
- Correlação moderada entre `TOTAL_ESCOLA` e as demais variáveis
- Região Nordeste apresenta outliers significativos

### 🎯 Insights Relevantes
- **Distrito Federal** destaca-se em matrículas por escola
- **Variação mínima** em verbas por matrícula entre UFs
- **Número de estudantes** é o principal parâmetro para repasse de verbas

### 🧮 Modelo Preditivo (após normalização de dados)
```python
# Equação do modelo final
VERBA = 9413061.1111 + 4105362.3470 × TOTAL_ESCOLA + 8741274.1531 × MATRICULAS
