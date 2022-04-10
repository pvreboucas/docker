# Docker: Criando containers sem dor de cabeça

[Curso de docker e docker compose da formação DevOps/Alura.](https://cursos.alura.com.br/course/docker-e-docker-compose)

[Principal](https://github.com/pvreboucas/docker/tree/main)

[Aula Anterior](https://github.com/pvreboucas/docker/tree/aula-1)


## Docker e DevOps ##


DevOps é um tópico bem amplo que envolve tanto aspectos culturais como técnicos, mas possui como principal objetivo aumentar a qualidade e eficiência da entrega de software. DevOps é uma metodologia que visa integrar os times de desenvolvimento com infraestrutura e o Docker está tendo um papel importante nessa tarefa.

Repare que com Docker os desenvolvedores não precisam se preocupar em configurar um ambiente de desenvolvimento específico de cada vez. Em vez disso, eles podem se concentrar na construção de um código de boa qualidade. Isso, obviamente, leva à aceleração nos esforços de desenvolvimento. O Docker facilita muito construir o ambiente: é rapido, simples e confiável.

No outro lado, para a equipe de operações de TI/Sysadmins, o Docker possibilita configurar ambientes que são exatamente como um servidor de produção e permite que qualquer pessoa trabalhe no mesmo projeto com exatamente as mesmas configurações, independentemente do ambiente de host local. As configurações são descritas em arquivos simples facilmente aplicáveis pelo desenvolvedor.

Com a padronização de um entregável Docker é possível que o desenvolvedor tenha um ambiente similar ao de produção na sua máquina sem todo o custo de configuração e o Sysadmin consiga lidar apenas com um tipo de entregável conseguindo, desta forma, dar atenção aos desafios de monitoramento e orquestração para que nada dê errado. Neste caso, o melhor para os dois.

## Consolidando o Conhecimento ##

Chegou a hora de você repetir todos os passos realizados por mim durante esta aula. Isto é:

* rodar o container ```dockersamples/static-site```
* mapear a porta usando o parâmetro ```-P``` ou ```-p```
* definir um nome para o container com o parâmetro ```--name```
* rodar o container no modo detached com o parâmetro ```-d```
* listar, parar e remover containers

Caso já tenha feito, excelente. Se ainda não, é importante que você execute o que foi visto no vídeo para poder continuar com o próximo capítulo.

No próximo capítulo veremos onde guardar os dados da aplicação de maneira segura. Aguarde!

## O que aprendemos? ##

Aprendemos neste capítulo:

* Comandos básicos do Docker para podermos baixar imagens e interagir com o container.
* Imagens do Docker possuem um sistema de arquivos em camadas (Layered File System) e os benefícios dessa abordagem principalmente para o download de novas imagens.
* Imagens são Read-Only sempre (apenas para leitura)
* Containers representam uma instância de uma imagem
* Como imagens são Read-Only os containers criam nova camada (layer) para guardar as alterações
* O comando Docker run e as possibilidades de execução de um container
 
Segue também uma breve lista dos comandos utilizados:

* ```docker ps``` - exibe todos os containers em execução no momento.
* ```docker ps -a``` - exibe todos os containers, independentemente de estarem em execução ou não.
* ```docker run -it NOME_DA_IMAGEM``` - conecta o terminal que estamos utilizando com o do container.
* ```docker start ID_CONTAINER``` - inicia o container com id em questão.
* ```docker stop ID_CONTAINER``` - interrompe o container com id em questão.
* ```docker start -a -i ID_CONTAINER``` - inicia o container com id em questão e integra os terminais, além de permitir interação entre ambos.
* ```docker rm ID_CONTAINER``` - remove o container com id em questão.
* ```docker container prune``` - remove todos os containers que estão parados.
* ```docker rmi NOME_DA_IMAGEM``` - remove a imagem passada como parâmetro.
* ```docker run -d -P --name NOME dockersamples/static-site``` - ao executar, dá um nome ao container.
* ```docker run -d -p 12345:80 dockersamples/static-site``` - define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345.
* ```docker run -d -P -e AUTHOR="Fulano" dockersamples/static-site``` - define uma variável de ambiente AUTHOR com o valor Fulano no container criado.

    
*[Próxima Aula](https://github.com/pvreboucas/docker/tree/aula-3)*
