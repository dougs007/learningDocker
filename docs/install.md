## Instalação do Docker no Linux Deepin

Instale gerenciadores de chaves e ferramentas relacionadas
2. $ sudo apt-get install apt-transport-https ca-certificates curl python-software-properties software-properties-common

Baixe e instale a chave 
3. curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -

Verifique se a chave está instalada com sucesso
4. sudo apt-key fingerprint 0EBFCD8

Se ocorrer tudo certo, exibirá a seguinte mensagem, ou algo semelhante:
pub 4096R/0EBFCD88 2017-02-22 Key fingerprint = 9DC8 5822 9FC7 DD38 854A E2D8 8D81 803C 0EBF CD88 
 uid Docker Release (CE deb) <docker@docker.com> 
 sub 4096R/F273FCD8 2017-02-22

Adicione também o repostitório oficial do Docker
5. sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian wheezy stable"

Atualize os pacotes
6. sudo apt-get update

Instale o Docker-ce
7. sudo apt-get install docker-ce

Verifique se o docker está instalado corretamente
8. sudo docker run hello-world


Turorial seguido na instalação:
https://medium.com/@wendreof/instalando-docker-no-linux-deepin-a48a3f9d9b8c