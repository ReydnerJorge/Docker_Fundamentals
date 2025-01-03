# curl -fsSL https://get.docker.com -o get-docker.sh
# sh get-docker.sh


# Iniciar o serviço do docker
-> systemctl start docker -> iniciar o docker

# Verificar o status
-> systemctl status docker

# baixar uma imagem do docker
-> docker pull ...
-> docker pull debian:9 => tag da versão

# Verificar as imagens baixadas
-> docker images

# Executar a imagem
-> docker run
-> docker container run
-> docker run -dti debian:9 =  subir container utilizando a tag
-> docker run -it (i- modo de interação / t- aloca um pseudo terminal)
-> docker run -d (deixar o container em background)
-> docker exec -it (id) (/bin/bash)

# Verificar a excução
-> docker ps > mostra quais conteiners estão em execução
-> docker container ls
-> docker ps -a > mostra quais conteiners foram executados recentes 

# Tempo de executção
-> docker run (selecionar a imagem) sleep 10 

# Para a execução
-> docker stop (id ou name do container)

# Deletar container / imagens
-> docker rm (id) deleta o container
-> docker rmi deleta a imagem

# Modificando o nome do container
-> docker run -dti --name Ubuntu-A ubuntu 

# Criar pastas e arquivos
-> docker exec Ubuntu-A mkdir /destino

# Verificar pastas dentro do container
-> docker exec Ubuntu-A ls /

# Copiar arquivos e pastas entre container`s
-> docker cp arquivo1.txt Ubuntu-A:/destino
-> docker exec Ubuntu-A ls /destino -l verificar se o arquivo foi para o destino

# Docker Help
-> docker --help
-> docker container --help