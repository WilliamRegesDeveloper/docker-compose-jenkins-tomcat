## Docker Compose com Jenkins e Tomcat
Esse script faz o pull da imagem da ferramenta de automação de builds e deploy, o Jenkins.


##Idéia
A idéia é fazer com que o jenkins faça builder de uma aplicação assim que um job
entender que foi feito commmit na branch master da aplicação que está logado 
em alguma ferramneta de versão. 

Assim que o job faz builder, o mesmo irá fazer deploy em um container Tomcat.
