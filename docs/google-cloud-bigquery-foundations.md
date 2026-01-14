# 🚀 Estudos em Google Cloud: BigQuery e Análise de Dados

Neste projeto, explorei os fundamentos de Computação em Nuvem utilizando o **Google BigQuery**. O objetivo foi unir o conhecimento técnico de SQL com a habilidade de comunicação clara e simplificada.

## 📽️ Analogia: O BigQuery e a Locadora de Filmes

Para entender o funcionamento e os custos do BigQuery, desenvolvi a seguinte analogia:

> Imagine que ele funciona de maneira semelhante às antigas locadoras de filmes, mas com pequenas diferenças. Se você alugar um filme de duração maior, pagará mais por ele. Porém se for um filme de duração menor, pagará menos, proporcionalmente ao tamanho de cada filme (como se fossem os arquivos que você pediu ao BigQuery para ler). Caso tenha dúvidas sobre qual 'filme' goste, pode pedir para o funcionário da locadora ler alguns títulos para você, o que te geraria um custo, mas provavelmente te traria mais assertividade na hora de escolher o que quer 'assistir'.

## 💡 Explicação Técnica (Mundo Real)

Saindo da analogia para a prática do BigQuery, as principais boas práticas que apliquei foram:

* **Eficiência de Custo:** É fundamental entender as ferramentas para evitar gastos desnecessários. O BigQuery permite filtrar arquivos de forma precisa. Mesmo que um dataset tenha 1TB, se filtrarmos para ler apenas 2 colunas, pagaremos apenas pelo processamento dessas colunas, ignorando o restante do tamanho do arquivo.
* **O perigo do SELECT:** Não recomendo em hipótese alguma o uso do comando `SELECT *`, pois ele força a leitura de todo o arquivo (ignorando filtros de coluna), o que resulta em um custo muito maior e desnecessário.

## 🛠️ Prática Realizada

Realizei uma consulta no dataset público de crimes de Austin/Texas, aplicando filtros inteligentes para garantir que a busca não retornasse vazia devido à sensibilidade de letras maiúsculas/minúsculas.

**Comando utilizado:**

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
**Exportação:** Os dados foram migrados para o **Google Sheets** e formatados como tabela para facilitar a leitura e apresentação.

## Conclusão e Boas Práticas:

Utilizei o comando **LIMIT 10** para otimizar o consumo, limitando a exibição a apenas 10 linhas e evitando desperdício de cota. Outro recurso essencial foi a função **UPPER**, que padroniza os dados em maiúsculas durante a busca. Isso resolve problemas de case sensitivity (diferença entre maiúsculas e minúsculas), garantindo que a consulta retorne resultados mesmo quando não sabemos exatamente como o dado foi inserido no banco.

Esses aprendizados foram consolidados através do treinamento **Capacita+: Aprenda IA com Google Cloud** e da trilha **Generative AI Leader** no portal **Google Skills**, seguindo as boas práticas oficiais da plataforma.

#bigquery #sql #google-cloud #technical-writing
