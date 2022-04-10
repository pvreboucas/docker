# Docker: Criando containers sem dor de cabeça

[Curso de docker e docker compose da formação DevOps/Alura.](https://cursos.alura.com.br/course/docker-e-docker-compose)

[Principal](https://github.com/pvreboucas/docker/tree/main)

[Aula Anterior](https://github.com/pvreboucas/docker/tree/aula-3)

## Consolidando o conhecimento ##



Chegou a hora de você seguir todos os passos realizados por mim durante esta aula. Isto é:

* criar e configurar um Dockerfile
* criar uma imagem através do seu Dockerfile
* criar um container a partir da sua imagem
* subir a imagem no Docker Hub

Caso já tenha feito, excelente. Se ainda não, é importante que você execute o que foi visto no vídeo para poder continuar com o próximo capítulo.

No próximo capítulo, veremos mais sobre a comunicação entre os containers. Vamos continuar?


## O que aprendemos? ##



Aprendemos neste capítulo:

* A entender o papel do arquivo DockerFile para criar imagens.
  *O Dockerfile define os comandos para executar instalações complexas e com características específicas.
* Vimos os principais comandos como ```FROM```, ```MAINTAINER```, ```COPY```, ```WORKDIR```, ```RUN```, ```EXPOSE``` e ```ENTRYPOINT```
* A subir uma imagem criada através de um Dockerfile para o Docker Hub e disponibilizar para os desenvolvedores

Lembrando também:

* as imagens são read-only sempre
* um container é uma instância de uma imagem
* para guardar as alterações a docker engine cria uma nova layer em cima da última layer da imagem

Segue também uma breve lista dos comandos utilizados:

* ```docker build -f Dockerfile``` - cria uma imagem a partir de um Dockerfile.
* ```docker build -f CAMINHO_DOCKERFILE/Dockerfile -t NOME_USUARIO/NOME_IMAGEM``` - constrói e nomeia uma imagem não-oficial informando o caminho para o Dockerfile.
* ```docker login``` - inicia o processo de login no Docker Hub.
* ```docker push NOME_USUARIO/NOME_IMAGEM``` - envia a imagem criada para o Docker Hub.
* ```docker pull NOME_USUARIO/NOME_IMAGEM``` - baixa a imagem desejada do Docker Hub.

[Próxima Aula](https://github.com/pvreboucas/docker/tree/aula-5)
