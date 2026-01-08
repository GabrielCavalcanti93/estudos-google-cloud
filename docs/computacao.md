# Guia de Computação: Google Cloud

Para criar uma instância de máquina virtual via Cloud Shell, utilize o seguinte comando:

```bash
gcloud compute instances create my-vm \
    --machine-type=n1-standard-1 \
    --zone=us-central1-a
```
Certique-se de selecionar corretamente o **ID do projeto** antes de iniciar a operação.
