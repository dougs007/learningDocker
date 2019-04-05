###### Ver a versão instalada do docker
>$ docker version

###### Baixar a imagem do hello-world 
>$ docker run hello-world

###### Listar os containers ativos
>$ docker ps

###### Listar todos os containers criados
>$ docker ps -a

###### Baixar a imagem do ubuntu e executa comandos no modo iterativo
>$ docker run -it ubuntu

###### Startar o container de ID {dd22} e Entrar no módo iterativo (-a = attach)
>$ docker start -a -i dd22

###### Remover o container de ID {dd22}
>$ docker rm dd22

###### Remover todos os containers docker
>$ docker container prune

###### Listar as imagens
>$ docker images

###### Remover a imagem passada no parâmetro (hello-world)
>$ docker rmi hello-world

###### Parar o container sem esperar os dez segundos default (-t=time 0= 0 seconds df2=container_id)
>$ docker stop -t 0 df2

###### Baixar imagem setando a porta (-P= port)
>$ docker run -d -P dockersamples/static-site

###### Baixar imagem setando o name (name= meu-site)
>$ docker run -d -P --name meu-site dockersamples/static-sitedocker run -d -P --name meu-site dockersamples/static-site

###### Baixar imagem setando variável de ambiente (-e= environment, AUTHOR= variavel)
>$ docker run -d -P -e AUTHOR="Douglas X" dockersamples/static-site

###### Listar apenas os id's dos containers ativos
>$ docker ps -q

###### Parar os containers ativos passando vários id's, com o time default como 0
>$ docker stop -t 0 $(docker ps -q)


### Perguntas frequentes.

1 ) O que é um container?


2 ) O que é uma imagem?


3 ) O que é um volume?
    É onde será contidos os volumes de dados da aplicação, sendo salvo numa pasta no dockerhub. Logo, toda
vez que você remover um container, ele não estará apagando todos os arquivos de log's, por causa que os mesmos
estão contidos ao dockerhub.

    3.1 ) Como um volume na máquina se conecta e faz para receber e enviar dados ao dockerhub ?

4 ) O que é um entrypoint no docker?


5 ) O que é workdir no docker?


### Comandos dentro do Dockerffile

###### Baixar uma imagem node com a última versão
> FROM node:latest

###### Informar o mantedor da imagem
> MAINTAINER Douglas Santana

###### Copiar o projeto todo para a pasta /var/www/
> COPY . /var/www

###### Executar o comando para instalar as dependências
> RUN npm install

###### Executar no caminho exibido (work directory)
> WORKDIR /var/www



## Comandos utilizados.


> docker build -f Dockerfile - cria uma imagem a partir de um Dockerfile.
> docker build -f CAMINHO_DOCKERFILE/Dockerfile -t NOME_USUARIO/NOME_IMAGEM - constrói e nomeia uma imagem
não-o cial informando o caminho para o Dockerfile.
> docker login - inicia o processo de login no Docker Hub.
> docker push NOME_USUARIO/NOME_IMAGEM - envia a imagem criada para o Docker Hub.
> docker pull NOME_USUARIO/NOME_IMAGEM - baixa a imagem desejada do Docker Hub.