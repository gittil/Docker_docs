#instale o docker pelo site oficial

https://www.docker.com/products/docker-desktop



#Acesse o link abaixo e siga as etapas do um ao cinco, bem tranquilo e bastante explicativo, não tem erro.
https://docs.microsoft.com/pt-br/windows/wsl/install-win10

https://docs.microsoft.com/pt-br/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package





#puxar imagem do cassandra
docker pull cassandra

#consultando imagens instaladas
docker images

#criar a pasta para arquivos persistentes
sudo mkdir /var/lib/cassandra -p


#criando um containner do cassandra
docker run --name cassandra -p 9042:9042 -v /var/lib/cassandra:/var/lib/cassandra -d cassandra

#usando o containner
docker exec -it cassandra bash

#entrando no prompt de comando do cassanda
cqlsh



#pull da imagem do MySQL
docker pull mysql

#criar a pasta para arquivos persistentes
mkdir /var/lib/mysql -p

#consultar conteudo da pasta
ls -la /var/lib/mysql

#criar o container
docker run -d --name mysql-server -p 3306:3306 -v /var/lib/mysql:/var/lib/mysql -e "MYSQL_ROOT_PASSWORD=admin123" mysql


#instalando o cliente MySQL localhost
apt-get install mysql-client

#acessando o serviço em execução no container docker
mysql -h 127.0.0.1 -u root -p

**https://techexpert.tips/pt-br/mysql-pt-br/mysql-instalacao-docker/

#listar containers instalados
docker container ls --all


docker pull jupyter/all-spark-notebook

docker run -p 4040:4040 -p 8888:8888 --name myjupyter 
-v $(pwd):/home/jovyan/work jupyter/all-spark-notebook

docker start <nome_do_contanier>
docker stop <nome_do_contanier>


