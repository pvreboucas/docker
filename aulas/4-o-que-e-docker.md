*[<< AULA ANTERIOR](https://github.com/pvreboucas/docker/blob/aula-1/aulas/3-era-dos-containers.md)*

Agora que já vimos a diferença entre máquinas virtuais e containers, chegou a hora de introduzirmos o Docker nesse contexto, que se divide entre duas coisas: a Docker, Inc., empresa que toma conta do Docker, e a tecnologia dos containers.

## Docker, Inc. ##

Primeiramente, devemos falar sobre a Docker, Inc., que no início era chamada de dotCloud. A dotCloud era uma empresa de PaaS (Platform as a Service), sendo responsável pela hospedagem da nossa aplicação, levantando o servidor, configurando-o, liberando portas, etc, fazendo tudo o que é necessário para subir a nossa aplicação. Outros exemplos de empresas de PaaS são o Heroku, Microsoft Azure e Google Cloud Platform.

Inicialmente, para prover a parte de infraestrutura, a dotCloud utilizava o Amazon Web Services (AWS), serviço que nos disponibiliza máquinas virtuais e físicas para trabalharmos. E para hospedar uma aplicação, sabemos que precisamos do sistema operacional, mas a dotCloud introduziu o conceito de containers na hora de subir uma aplicação, dando origem ao Docker, tecnologia utilizada para baratear o custo de hospedar várias aplicações em uma mesma máquina.

Ou seja, quando a dotCloud criou o Docker, sua intenção era economizar os gastos da empresa, subindo várias aplicações em containers, em um mesmo hardware do AWS, e com o passar do tempo a empresa percebeu que tinham muitos desenvolvedores interessados na tecnologia que ela havia criado, a tecnologia que permite a criação de containers, que faz o intermédio entre eles e o sistema operacional, o Docker.

## As tecnologias do Docker ##

O Docker nada mais é do que uma coleção de tecnologias para facilitar o deploy e a execução das nossas aplicações. A sua principal tecnologia é a Docker Engine, a plataforma que segura os containers, fazendo o intermédio entre o sistema operacional.

Outras tecnologias do Docker que facilitam a nossa vida e que veremos neste curso são o Docker Compose, um jeito fácil de definir e orquestrar múltiplos containers; o Docker Swarm, uma ferramenta para colocar múltiplos docker engines para trabalharem juntos em um cluster; o Docker Hub, um repositório com mais de 250 mil imagens diferentes para os nossos containers; e a Docker Machine, uma ferramenta que nos permite gerenciar o Docker em um host virtual.

## Open Source ##

Quando a empresa dotCloud tornou-se a Docker, Inc., focada em manter o Docker, ela o abriu para o mundo open source, tudo disponibilizado no seu [GitHub](https://github.com/docker), inclusive com várias empresas contribuindo para o desenvolvimento dessa tecnologia.

Apesar de haver alguns serviços pagos, em sua grande parte a tecnologia do Docker é uma tecnologia open source, utilizada por várias empresas. Então, vamos colocar as mãos na massa e aprender a instalar o Docker nas próximas aulas.

*[PRÓXIMA AULA >>]()*
