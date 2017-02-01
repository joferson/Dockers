![Docker logo](wp-logo.png "Docker")

#### Como Instalar o Docker? ####

* Docker [Releases](https://github.com/docker/docker/releases)

        wget -qO- https://get.docker.com/ | sh
    
  ### Utilitários

    * Docker Machine [Releases](https://github.com/docker/machine/releases) 

            $ curl -L https://github.com/docker/machine/releases/download/v0.9.0/docker-machine-`uname -s`-`uname -m` >/tmp/docker-machine &&
                chmod +x /tmp/docker-machine &&
                sudo cp /tmp/docker-machine /usr/local/bin/docker-machine
    	
    * Docker Compose [Releases](https://github.com/docker/compose/releases) 
         
            $ pip install docker-compose
        ou    	
         
            $ curl -L https://github.com/docker/compose/releases/download/1.10.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
            chmod +x /usr/local/bin/docker-compose

### Docker  ###


#### Tá, e agora, como eu uso isso? ####

LEIA O MANUAL -  [TL;DR - user guide](https://docs.docker.com/engine/userguide/) :-P


* Utilize o comando **images** para listar:

        docker images

* Como remover imagens locais?

        docker rmi <CONTAINER_ID>
        
* Utilize o comando **search** para listar as images disponíveis:

        docker search ubuntu

* Encontrado a imagem correta, utilize **pull** para baixar:
        
        docker pull ubuntu

* Listar containers ativos:

        docker ps

* Executar um container:

        docker run -it ubuntu /bin/bash
        
* Entrar em um container em ativo:
        
        docker exec -it ubuntu /bin/bash