# Tradução Técnica: Dataset Público de Raios (NOAA)

> **Nota de Localização:** Este documento é uma tradução técnica e adaptação para fins de portfólio.
> **Fonte Original:** [Google Cloud Marketplace - Lightning Dataset](https://console.cloud.google.com/marketplace/product/noaa-public/lightning?hl=pt-br)

Este conjunto de dados contém informações meteorológicas coletadas pela [Vaisala](https://www.vaisala.com/en/products/national-lightning-detection-network-nldn) (VNLDN) e agregadas em quadrantes de 0.1° x 0.1° pelos especialistas do Centro Nacional de Informações sobre o Meio Ambiente (NCEI), como parte de um banco de dados abrangente sobre chuvas intensas.

Os dados apresentam o histórico de incidência de raios agregados em **quadrantes (tiles)** com um raio de redistribuição de aproximadamente 11 km. O dataset informa o número de raios por dia, bem como o **epicentro de cada quadrante**. As consultas abaixo demonstram como utilizar os recursos de **GIS (Sistema de Informação Geográfica)** do BigQuery para analisar esses dados. Para mais detalhes, consulte a [documentação do BigQuery GIS](https://docs.cloud.google.com/bigquery/docs/geospatial-intro?hl=pt_BR).

### Disponibilidade dos Dados
Os registros iniciam em 1987 e são atualizados continuamente (com atraso de alguns dias para processamento). Para monitoramento em tempo real de raios entre nuvens e solo, acesse o [Dataset NOAA GOES-16](https://console.cloud.google.com/bigquery?p=bigquery-public-data&d=noaa_goes16). Em breve, o sistema GOES-17 também estará disponível para cobertura do hemisfério ocidental.

### Custos e Acesso
Estes dados integram o nível gratuito do BigQuery, que oferece **1 TB de processamento por mês**. Isso permite que cada usuário execute consultas neste dataset sem custos mensais, dentro desse limite. Assista a este vídeo curto: [O que é o BigQuery?](https://docs.cloud.google.com/bigquery/docs/introduction?hl=pt_BR).

### Exemplos de Consultas (Sample Queries)
Tente executar as consultas abaixo na interface (UI) do BigQuery:

1. **Quais áreas (CEPs) dos EUA possuem mais incidências de raios?**
   Utilizando o BigQuery GIS, cruzamos os dados de raios com polígonos de CEPs (Zip Code Tabulation Areas) para determinar as áreas mais atingidas desde 2018. Saiba mais no [Marketplace](https://console.cloud.google.com/marketplace/details/bigquery-public-data/zipcode_area).
   * [Executar esta consulta](https://console.cloud.google.com/bigquery?sq=1073493072202:4f200a2efb26468f9d97ffb65cbd7072)

2. **Qual dia do ano 2000 registrou mais raios nos EUA?**
   Esta consulta agrega o total de raios por dia e retorna os 10 dias com maior volume de ocorrências.

### Termos de Serviço
Este dataset é público e segue a [Política de Dados do Data.gov](http://www.data.gov/privacy-policy#data_policy). Os dados são fornecidos **"no estado em que se encontram" (As Is)**, sem garantias explícitas ou implícitas pelo Google, que não se responsabiliza por danos decorrentes do uso das informações.
