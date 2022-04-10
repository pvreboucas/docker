*[<< AULA ANTERIOR](https://github.com/pvreboucas/docker/blob/aula-1/aulas/4-o-que-e-docker.md)*

Como o Docker é uma aplicação que se liga fortemente ao sistema operacional e é dependente de várias de suas funcionalidades, a instalação para cada um dos sistemas operacionais é diferente, e vamos abordar o caso do Windows neste vídeo.

## Instalação principal no Windows ##

Existem duas possibilidades para instalar o Docker no Windows. Temos a principal, utilizando o [Docker for Windows](https://store.docker.com/editions/community/docker-ce-desktop-windows), no qual podemos baixar o instalador [clicando aqui](https://download.docker.com/win/stable/InstallDocker.msi) e a alternativa, utilizando o Docker Toolbox, que veremos daqui a pouco.

Primeiramente, devemos nos atentar aos requisitos do uso do Docker for Windows, ou seja, devemos possuir um Windows com:

* Arquitetura 64 bits
* Versão Pro, Enterprise ou Education.
* Virtualização habilitada

Em relação a este último ponto, o Windows por padrão já deixa a virtualização habilitada, podemos conferir acessando o Gerenciador de Tarefas, e indo na aba Performance:

![01](https://github.com/pvreboucas/docker/blob/aula-1/aulas/imagens/5-1-virtualizacao-habilitada.png)

```
Se no seu caso a virtualização não estiver habilitada, por favor poste no 
fórum do curso a versão do seu Windows e modelo do seu computador para tentarmos ajudá-lo 
pois cada fabricante de Hardware configura isto de modos diferentes.
```

Seguimos o passo a passo do instalador para aceitar a licença, autorizamos o instalador e seguimos com a instalação. Ao clicar em Finish, precisamos encerrar a sessão do Windows e iniciá-la novamente. Ao fazer o login, precisamos habilitar o Hyper-V, clicando em Ok, para que o computador será reiniciado.

Quando o computador terminar a reinicialização, irá aparecer um ícone do Docker na barra inferior, à direita, ao lado do relógio. O Docker pode demorar um pouco para inicializar, mas quando a mensagem Docker is running for exibida, significa que ele foi instalado com sucesso e já podemos utilizá-lo.

## Funcionamento do Docker no Windows ##

O Docker é executado em cima de uma micromáquina virtual, chamada Alpine Linux, onde será executada a sua Docker Engine:

![02](https://github.com/pvreboucas/docker/blob/aula-1/aulas/imagens/5-2-docker-windows.png)

Mas para criar máquinas virtuais, o Docker precisa utilizar uma tecnologia chamada de Hyper-V, que é um Hypervisor. O problema disto é que o Hyper-V só está presente nas versões Professional, Education e Enterprise, ou seja, a maioria dos usuários comuns, que utilizam a versão Home Edition, não poderão instalar o Docker pelo modo tradicional, e terá que utilizar o Docker Toolbox.

Além disto, a principal ferramenta de instalação , o Docker for Windows necessita que você esteja utilizando um Windows 10 - 64 bits, com uma das versões citadas acima.

Vamos agora então detalhar o processo de instalação para cada esse caso.

## Instalação alternativa no Windows ##

Para instalar o Docker Toolbox, primeiramente devemos baixá-lo [aqui](https://download.docker.com/win/stable/DockerToolbox.exe). Ainda assim, precisamos garantir que o nosso Windows seja 64bits e que ele tenha a virtualização habilitada.

O Docker Toolbox vai instalar tudo que é necessário para que trabalhemos com o Docker em nosso computador, pois ele irá instalar também a Oracle VirtualBox, a máquina virtual da Oracle que vai permitir executarmos o Docker sem maiores problemas.

A diferença é que, quando trabalhamos com o Docker for Windows, podemos utilizar o terminal nativo do Windows, já no Docker Toolbox, ele instalará o Docker Machine, que deverá ser utilizado no lugar do terminal nativo do Windows.

*[PRÓXIMA AULA >>]()*
