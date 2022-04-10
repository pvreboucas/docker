# Docker: Criando containers sem dor de cabeça

[Curso de docker e docker compose da formação DevOps/Alura.](https://cursos.alura.com.br/course/docker-e-docker-compose)

[Principal](https://github.com/pvreboucas/docker/tree/main)



Vamos agora detalhar o processo de instalação do Docker Desktop for Windows e do Docker Toolbox.

## Instalando com Docker Desktop for Windows ##

Primeiramente você deve se atentar aos requisitos do uso do Docker Desktop for Windows, ou seja, deve possuir um Windows com:

* Arquitetura 64 bits
* Versão Pro, Enterprise ou Education.
* Virtualização habilitada

Em relação a este último ponto, o Windows por padrão já deixa a virtualização habilitada, mas você pode conferir acessando o Gerenciador de Tarefas, e indo na aba Performance:

```
Verificando se a virtualização está habilitada
```

*Se no seu caso a virtualização não estiver habilitada, por favor poste no fórum do curso a versão do seu Windows e modelo do seu computador para tentarmos ajudá-lo pois cada fabricante de Hardware configura isto de modos diferentes*

Na página do [Docker Desktop for Windows](https://www.docker.com/products/docker-desktop), baixe o instalador [clicando aqui](https://download.docker.com/win/stable/Docker%20for%20Windows%20Installer.exe). Siga o passo a passo do instalador para aceitar a licença, autorize o instalador e siga com a instalação. Ao clicar em Finish, encerre a sessão do Windows e inicie-a novamente. Ao fazer o login, habilitar o Hyper-V, clicando em Ok, para que o computador seja reiniciado.

Quando o computador terminar a reinicialização, irá aparecer um ícone do Docker na barra inferior, à direita, ao lado do relógio. O Docker pode demorar um pouco para inicializar, mas quando a mensagem *Docker is running* for exibida, significa que ele foi instalado com sucesso e você já pode utilizá-lo.

## Instalando com Docker Toolbox ##

Para instalar o Docker Toolbox, primeiramente baixe-o [aqui](https://download.docker.com/win/stable/DockerToolbox.exe). Ainda assim, garanta que o seu Windows seja 64bits e que ele tenha a virtualização habilitada.

O Docker Toolbox vai instalar tudo que é necessário para que você possa trabalhar com o Docker em seu computador, pois ele irá instalar também a Oracle VirtualBox, a máquina virtual da Oracle que vai permitir executar o Docker sem maiores problemas.

A diferença é que, quando você trabalha com o Docker Desktop for Windows, você pode utilizar o terminal nativo do Windows, já no Docker Toolbox, ele instalará o Docker Machine, que deverá ser utilizado no lugar do terminal nativo do Windows.

Vamos agora detalhar o processo de instalação do Docker for Mac e do Docker Toolbox.

## Instalando com Docker for Mac ##

Primeiramente você deve se atentar aos requisitos do uso do Docker for Mac, ou seja, deve possuir um macOS:

* Modelo 2010 ou mais recente
* Versão OS X El Capitan 10.11 ou mais recente
* Com no mínimo 4GB de memória RAM
* Sem VirtualBox instalada na versão 4.3.30 ou anterior, pois causa incompatibilidade com o Docker

A página dos requisitos pode ser acessada [aqui](https://docs.docker.com/desktop/mac/install/).

Na página do [Docker for Mac](https://docs.docker.com/desktop/mac/install/), baixe o instalador [clicando aqui](https://download.docker.com/mac/stable/Docker.dmg). Instale o Docker, clicando no .dmg baixado anteriormente e arrastando o Docker para as aplicações. Após isso, pesquise pelo Docker, confirme que quer utilizá-lo e dê acesso privilegiado a ele, clicando em OK e digitando a senha de administrador em seguida.

No menu superior do macOS, à direita, o ícone do Docker aparecerá. Ele pode demorar um pouco para inicializar, mas quando a mensagem Docker is now up and running! for exibida, significa que ele já pode ser utilizado.

## Instalando com Docker Toolbox ##

Para instalar o Docker Toolbox, primeiramente baixe-o [aqui](https://download.docker.com/mac/stable/DockerToolbox.pkg). 

O Docker Toolbox vai instalar tudo que é necessário para que você possa trabalhar com o Docker em seu computador, pois ele irá instalar também a Oracle VirtualBox, a máquina virtual da Oracle que vai permitir executar o Docker sem maiores problemas.

A diferença é que, quando você trabalha com o Docker for Mac, você pode utilizar o terminal nativo do macOS, pois o terminal está sendo executado dentro do próprio sistema operacional. Já no Docker Toolbox, ele instalará o Docker Machine, que deverá ser utilizado no lugar do terminal nativo do macOS.

## Instalando Docker no Ubuntu ##

Neste passo-a-passo, será visto como instalar o Docker no Ubuntu 64 bits. Todos os comandos listados devem ser executados no seu terminal.

Antes de mais nada, remova possíveis versões antigas do Docker:

```shell
sudo apt-get remove docker docker-engine docker.io
```

Depois, atualize o banco de dados de pacotes:

```shell
sudo apt-get update
```

Agora, adicione ao sistema a chave GPG oficial do repositório do Docker:

```shell
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

Adicione o repositório do Docker às fontes do APT:

```shell
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

Atualize o banco de dados de pacotes, para ter acesso aos pacotes do Docker a partir do novo repositório adicionado:

```shell
sudo apt-get update
```

Por fim, instale o pacote docker-ce:


```shell
sudo apt-get install docker-ce
```

Caso você queira, você pode verificar se o Docker foi instalado corretamente verificando a sua versão:


```shell
sudo docker version
```

E para executar o Docker sem precisar de sudo, adicione o seu usuário ao grupo docker:


```shell
sudo usermod -aG docker $(whoami)
```



Chegou a hora de você seguir todos os passos realizados por mim durante esta aula, isto é:

* instalar o Docker para seu sistema operacional
* executar o "Hello World" com Docker.

Caso já tenha feito, excelente. Se ainda não, é importante que você execute o que foi visto no vídeo para poder continuar com o próximo capítulo.

No próximo capítulo veremos como trabalhar com imagens. Te encontro lá!

## Uma Alternativa Online: Utilizando o Play With Docker ##

Não se desespere caso você tenha tido algum problema em instalar o Docker em sua máquina, você também tem a opção de utilizar o [Play With Docker](https://labs.play-with-docker.com/). Nele você poderá utilizar os comandos vistos daqui em diante e testar as diversas funcionalidades que o Docker proporciona. Ao acessar o site basta clicar em +Add New Instance e começar a utilizá-lo como estivesse usando sua máquina normalmente.


[Próxima Aula](https://github.com/pvreboucas/docker/tree/aula-2)
