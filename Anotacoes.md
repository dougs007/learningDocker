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

1) O que é um container?


2) O que é uma imagem?


3) O que é um volume?

