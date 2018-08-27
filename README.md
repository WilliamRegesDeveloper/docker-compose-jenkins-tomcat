## Docker Compose com Jenkins e Tomcat
Através da execução do arquivo docker-compose em ambiente docker pode-se subir um ambiente pré
configurado de servidores conteinizados com Jenkins e Tomcat.


## Proposta
A proposta inicial do projeto é criar um ambiente onde possa ser utilizado Jenkins como CI/CD. E o 
servidor de aplicação é o tomcat. Para que o funcionamento de builder e deploy no tomcat tenha efeito 
é necessário configurar um job no jenkins.
O job é configurado para clonar projetos do git, buildar, testar e fazer deploy em qualquer servidor de aplicação,
como o tomcat por exemplo.

## Rodando projeto em clurster Swarm
1. Crei um cluster utlizando Docker Swarm e faça clone no repositorio:
# $ docker swarm init --advertise-addr <ip-servidor>

2. Faça clone do projeto no repositório:
### $ git clone https://github.com/WilliamRegesDeveloper/docker-compose-jenkins-tomcat.git;

3. Entre no projeto docker-compose-jenkins-tomcat clonado e rode o comando para subir os stacks de servidores configurados no arquivo docker-service3.yml:
### $ docker stack deploy --compose-file docker-service3.yml servico-docker

3. Veja os serviços rodando:
### $ docker service ls

4. Entre nos serviços pelas portas externas já configuradas no arquivo docker-service3.yml:
* porta 8080 - login: sysdba; senha: masterkey;
* porta 50001 - Acesso ao serviço Jenkins;


## Entendendo o Jenkins

* Site oficial do [Jenkins](https://jenkins.io/).


