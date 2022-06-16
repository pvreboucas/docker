#  Docker Cheat Sheet - Os Comandos Utilizados #


Segue a lista com os principais comandos utilizados durante o curso:

* Comandos relacionados às informações
  * __```docker version```__ - exibe a versão do docker que está instalada.
  * __```docker inspect ID_CONTAINER```__ - retorna diversas informações sobre o container.
  * __```docker ps```__ - exibe todos os containers em execução no momento.
  * __```docker ps -a```__ - exibe todos os containers, independentemente de estarem em execução ou não.

* Comandos relacionados à execução
  * __```docker run NOME_DA_IMAGEM```__ - cria um container com a respectiva imagem passada como parâmetro.
  * __```docker run -it NOME_DA_IMAGEM```__ - conecta o terminal que estamos utilizando com o do container.
  * __```docker run -d -P --name NOME dockersamples/static-site```__ - ao executar, dá um nome ao container e define uma porta aleatória.
  * __```docker run -d -p 12345:80 dockersamples/static-site```__ - define uma porta específica para ser atribuída à porta 80 do container, neste caso 12345.
  * __```docker run -v "CAMINHO_VOLUME" NOME_DA_IMAGEM```__ - cria um volume no respectivo caminho do container.
  * __```docker run -it --name NOME_CONTAINER --network NOME_DA_REDE NOME_IMAGEM```__ - cria um container especificando seu nome e qual rede deverá ser usada.

* Comandos relacionados à inicialização/interrupção
  * __```docker start ID_CONTAINER```__ - inicia o container com id em questão.
  * __```docker start -a -i ID_CONTAINER```__ - inicia o container com id em questão e integra os terminais, além de permitir interação entre ambos.
  * __```docker stop ID_CONTAINER```__ - interrompe o container com id em questão.

* Comandos relacionados à remoção
  * __```docker rm ID_CONTAINER```__ - remove o container com id em questão.
  * __```docker container prune```__ - remove todos os containers que estão parados.
  * __```docker rmi NOME_DA_IMAGEM```__ - remove a imagem passada como parâmetro.

* Comandos relacionados à construção de Dockerfile
  * __```docker build -f Dockerfile```__ - cria uma imagem a partir de um Dockerfile.
  * __```docker build -f Dockerfile -t NOME_USUARIO/NOME_IMAGEM```__ - constrói e nomeia uma imagem não-oficial.
  * __```docker build -f Dockerfile -t NOME_USUARIO/NOME_IMAGEM CAMINHO_DOCKERFILE```__ - constrói e nomeia uma imagem não-oficial informando o caminho para o Dockerfile.

* Comandos relacionados ao Docker Hub
  * __```docker login```__ - inicia o processo de login no Docker Hub.
  * __```docker push NOME_USUARIO/NOME_IMAGEM```__ - envia a imagem criada para o Docker Hub.
  * __```docker pull NOME_USUARIO/NOME_IMAGEM```__ - baixa a imagem desejada do Docker Hub.

* Comandos relacionados à rede
  * __```hostname -i```__ - mostra o ip atribuído ao container pelo docker (funciona apenas dentro do container).
  * __```docker network create --driver bridge NOME_DA_REDE```__ - cria uma rede especificando o driver desejado.

* Comandos relacionados ao docker-compose
  * __```docker-compose build```__ - Realiza o build dos serviços relacionados ao arquivo docker-compose.yml, assim como verifica a sua sintaxe.
  * __```docker-compose up```__ - Sobe todos os containers relacionados ao docker-compose, desde que o build já tenha sido executado.
  * __```docker-compose down```__ - Para todos os serviços em execução que estejam relacionados ao arquivo docker-compose.yml.

