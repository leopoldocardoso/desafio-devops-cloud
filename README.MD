# Desafio Devops Cloud

## Objetivo do Desafio - Aula 1: Criar um ambiente docker para uma aplicação demo desenvolvida em python.

### Passo a passo realizado para concluir o desafio:

- Configurar docker na máquina local.
- Criar um dockerfile.
- Executar contêiner a partir da imagem gerada e garantir que aplicação esteja acessível na porta 5000.
- Enviar a imagem para o Dockerhub

### Print da aplicação em funcionamento

| ![conversao-distancia.png](/conversao-distancia/images/conversao-distancia.png) |
|:-----------------------------:|
| Figura 1 |

-----

## Objetivo do Desafio - Aula 2: Configurar um cluster kubernetes local utilizando k3d

### Passo a passo realizado para concluir o desafio:

- Instalação do cluster k3d no Linux utilizando o comando:

  ``` wget -q -O - https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash ```

- Criação do cluster k3d utilizando o comando:

  ``` k3d cluster create cluster-dev ```

- Criar o manifesto deployment.yaml para a aplicação conversao-distancia fosse executada em um ambiente kubernetes. Link do manifesto abaixo:

  Link do manifesto: [manifesto conversao-distancia](https://github.com/leopoldocardoso/desafio-devops-cloud/tree/main/k8s)

- Criar o Deployment com o comando:

  ``` kubectl create -f k8s/deployment.yaml ```

### Print do deployment, do pod em execução no cluster

| ![deployment.png](/conversao-distancia/images/deployment.png) |
|:-----------------------------:|
| Figura 2 |