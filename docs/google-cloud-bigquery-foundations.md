# 🚀 Estudos em Google Cloud: BigQuery

Neste projeto, explorei os fundamentos de **Cloud Computing** utilizando o **Google BigQuery**.

## 📽️ Analogia: A Locadora de Filmes
Para entender os custos do BigQuery, desenvolvi a seguinte analogia:

> Imagine que ele funciona como uma locadora. Se alugar um filme maior, pagará mais. Se for menor, pagará menos, proporcionalmente ao tamanho (arquivos lidos).

## 💡 Prática e Boas Práticas

* **Eficiência:** Filtrei apenas 2 colunas para economizar processamento.
* **Cuidado:** Evitei o `SELECT *` para não ler o arquivo inteiro sem necessidade.

## 🛠️ Comando SQL Utilizado

```sql
SELECT 
    primary_type, 
    description,
    timestamp
FROM 
    `bigquery-public-data.austin_crime.crime`
WHERE 
    UPPER(primary_type) LIKE '%THEFT%'
LIMIT 10

```

## 📊 Resultados
**Processamento:** A query foi otimizada para ler apenas o necessário.
**Exportação:** Os dados foram migrados para o Google Sheets e formatados como tabela para facilitar a leitura e apresentação.

**Conclusão e Boas Práticas:**
Utilizei o comando **LIMIT 10** para otimizar o consumo, limitando a exibição a apenas 10 linhas e evitando desperdício de cota. Outro recurso essencial foi a função **UPPER**, que padroniza os dados em maiúsculas durante a busca. Isso resolve problemas de case sensitivity (diferença entre maiúsculas e minúsculas), garantindo que a consulta retorne resultados mesmo quando não sabemos exatamente como o dado foi inserido no banco.


Esses aprendizados foram consolidados através do treinamento **Capacita+: Aprenda IA** com **Google Cloud** e da trilha **Generative AI Leader** no portal **Google Skills.**

#bigquery #sql #google-cloud #technical-writing
