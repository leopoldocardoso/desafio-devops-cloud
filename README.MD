# Desafio Devops Cloud

## Objetivo do Desafio - Aula 1: Criar um ambiente docker para uma aplicação demo desenvolvida em python.

### Passo a passo realizado para concluir o desafio:

- Configurar docker na máquina local.
- Criar um dockerfile.
- Executar contêiner a partir da imagem gerada e garantir que aplicação esteja acessível na porta 5000.
- Enviar a imagem para o Dockerhub.
- Link da imagem conversao-distancia no Dockerhub: https://hub.docker.com/repository/docker/leopoldopeixoto/conversao-distancia/general

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

  Link do manifesto: [manifesto conversao-distancia](https://github.com/leopoldocardoso/desafio-devops-cloud/tree/main/conversao-distancia/k8s)

- Criar o Deployment com o comando:

  ``` kubectl create -f k8s/deployment.yaml ```

### Print do deployment, do pod em execução no cluster

| ![deployment.png](/conversao-distancia/images/deployment.png) |
|:-----------------------------:|
| Figura 2 |


## Objetivo do Desafio - Aula 3: Criar um cluster kubernetes(EKS) na AWS e realizar deploy da aplicação fakeshop neste cluster

### Passo a passo realizado para concluir o desafio:

- Acesso a conta AWS.
- Criação de uma VPC para ser utilizada pelo cluster usando Cloud AWS Formation.
- Realizado Criação do Cluster EKS através da console AWS.
- Criação de imagem docker com aplicação fake-shop. 
  - Esta aplicação é feita em python
  - Utiliza banco de dados postgres que está sendo executado no EKS.
- Criação do manifesto de deployment utilizando a imagem criada anteriormente.
- Realização do deployment da aplicação no cluster kubernetes - EKS.
- Link da imagem da aplicação fake-shop no Dockerhub: https://hub.docker.com/repository/docker/leopoldopeixoto/fake-shop/general

# Print da aplicação

| ![deployment.png](/fake-shop/images/deployment.png) |
|:-----------------------------:|
| Figura 3 |


| ![aplicacao.png](/fake-shop/images/aplicacao.png) |
|:-----------------------------:|
| Figura 4 |
