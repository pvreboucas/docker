# Docker: Criando containers sem dor de cabeça

[Curso de docker e docker compose da formação DevOps/Alura.](https://cursos.alura.com.br/course/docker-e-docker-compose)

[Principal](https://github.com/pvreboucas/docker/tree/main)

[Aula Anterior](https://github.com/pvreboucas/docker/tree/aula-4)


## Sobre o comando pull ##

No último video usei o comando ```docker pull douglasq/alura-books:cap05``` sem ter explicado antes. Fique tranquilo pois esse comando faz nada mais do que baixar, sem rodar, a imagem desejada do Docker Hub :)

Por exemplo, para baixar a imagem ubuntu do Docker Hub você pode usar:

```bash
docker pull ubuntu
```

Isso é diferente do comando ```run```, que baixa a imagem (se não existe local) e depois cria e roda o container. O ```pull``` apenas baixa!

Para baixar uma imagem de um usuário especifico vimos a sintaxe:

```bash
docker pull NOME_USUARIO/NOME_IMAGEM
```

Além disso, uma imagem pode ter um tag que serve para pegar uma determinada versão dessa imagem. Alias, você já viu a tag ```:latest``` e no video eu usei a tag ```:cap05```, por exemplo:

```bash
docker pull douglasq/alura-books:cap05
```

Isso baixará a versão (ou tag) cap05 da imagem alura-books do usuário douglasq.

## Consolidando seu conhecimento ##

Chegou a hora de você seguir todos os passos realizados por mim durante esta aula. Isto é:

* criar a sua própria rede do Docker
* pegar dados de um banco em um outro container

Caso já tenha feito, excelente. Se ainda não, é importante que você execute o que foi visto no vídeo para poder continuar com o próximo capítulo.

Bora usar e aprender Docker!!

## O que aprendemos? ##


Neste capítulo aprendemos:

* Que imagens criadas pelo Docker acessam a mesma rede, porém apenas através de IP.
* Ao criar uma rede é possível realizar a comunicação entre os containers através do seu nome.
* Que durante a criação de uma rede precisamos indicar qual driver utilizaremos, geralmente, o driver ```bridge```. 

Segue também uma breve lista dos comandos utilizados:

* ```hostname -i``` - mostra o ip atribuído ao container pelo docker (funciona apenas dentro do container).
* ```docker network create --driver bridge NOME_DA_REDE``` - cria uma rede especificando o driver desejado.
* ```docker run -it --name NOME_CONTAINER --network NOME_DA_REDE NOME_IMAGEM``` - cria um container especificando seu nome e qual rede deverá ser usada.



[Próxima Aula](https://github.com/pvreboucas/docker/tree/aula-6)
