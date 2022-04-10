# Docker: Criando containers sem dor de cabeça

[Curso de docker e docker compose da formação DevOps/Alura.](https://cursos.alura.com.br/course/docker-e-docker-compose)

[Principal](https://github.com/pvreboucas/docker/tree/main)

[Aula Anterior](https://github.com/pvreboucas/docker/tree/aula-2)


## Consolidando o conhecimento ##


Chegou a hora de você seguir todos os passos realizados por mim durante esta aula. Isto é:

* trabalhar com o Docker Host, para criar um volume
* salvar dados no volume criado
* rodar um código em um container

Caso já tenha feito, excelente. Se ainda não, é importante que você execute o que foi visto no vídeo para poder continuar com o próximo capítulo.

No próximo capítulo construiremos as nossas próprias imagens com Docker. Vamos continuar?


## O que aprendemos? ##



Nessas aulas avançamos bastante e aprendemos:

* Que containers são voláteis, isso é, ao remover um, removemos os dados juntos
* Para deixar os dados persistente devemos usar Volumes
* Que volumes salvos não ficam no container e sim no Docker Host
* Como criar um ambiente de execução node.js

Segue também uma breve lista dos comandos utilizados:

* ```docker run -v "[CAMINHO_VOLUME_LOCAL:]CAMINHO_VOLUME_CONTAINER" NOME_DA_IMAGEM``` - cria um volume no respectivo caminho do container, caso seja especificado um caminho local monta o volume local no volume do container.
* ```docker inspect ID_CONTAINER``` - retorna diversas informações sobre o container.


[Próxima Aula](https://github.com/pvreboucas/docker/tree/aula-4)
