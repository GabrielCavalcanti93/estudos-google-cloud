# Guia de Banco de Dados: Google Cloud SQL

O Cloud SQL é um serviço de banco de dados relacional totalmente gerenciado para MySQL, PostgreSQL e SQL Server.

### Criando uma Instância MySQL
Para criar uma instância básica via Cloud Shell, utilize o comando abaixo:

```bash
gcloud sql instances create minha-instancia \
    --database-version=MYSQL_8_0 \
    --tier=db-f1-micro \
    --region=us-central1
```
