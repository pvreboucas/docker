*[<< AULA ANTERIOR](https://github.com/pvreboucas/docker/blob/aula-1/aulas/6-instalando-docker-no-macos.md)*

Com o Docker instalado no nosso sistema operacional (seja ele qual for), já podemos testá-lo para ver o seu funcionamento.

Se o nosso Docker foi instalado pelo Docker for Mac ou Docker for Windows, conseguimos executar os seus comandos através do terminal nativo do Mac ou do Windows (Prompt de Comando). Mas se o nosso Docker foi instalado pelo Docker Toolbox, devemos executar os seus comandos através do Docker Quickstart Terminal, terminal que foi instalado pelo próprio Docker Toolbox.

Então, vamos abrir um terminal que consiga se comunicar com o nosso Docker, e executar o seguinte comando para verificar a sua versão:

```bash
docker version
```

Também podemos executar o clássico Hello World:

```bash
docker run hello-world
```

Ao executar o comando, a primeira mensagem impressa é:

```bash
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
```

Ou seja, o Docker não conseguiu achar a imagem localmente, e ele foi em algum lugar e a baixou. Como assim? Quando executamos o comando docker run hello-world, estamos dizendo para o Docker criar um container com a imagem do hello-world. Como não possuímos essa imagem localmente, ele foi buscá-la no Docker Hub, repositório do próprio Docker com várias imagens para utilizarmos em nossos projetos.

Baixada a imagem, ela é executada, exibindo a seguinte mensagem:

```bash
Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://cloud.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/engine/userguide/
```

Na mensagem, é detalhado o que foi feito para a execução da imagem. O nosso Docker local entrou em contato com a Docker Engine, que por sua vez baixou a imagem hello-world do Docker Hub, criou um container com ela e a executou. Após isso, a saída é impressa para nós e a imagem é encerrada.

Esses passos descritos, imagem, container, seus ciclos de vida, tudo isso veremos ao longo dos próximos capítulos.


*[PRÓXIMA AULA >>](https://github.com/pvreboucas/docker/blob/aula-2/aulas/1-comandos-basicos-com-containers.md)*
