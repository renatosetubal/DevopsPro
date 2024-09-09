# Desafio 01 - Banco de Dados PostgreSQL
## ✨Tarefa: ✨
  
Você está dando os primeiros passos no uso de containers. E a melhor forma de iniciar no mundo de containers é usar em ambiente de desenvolvimento.

Sua missão é ajudar a equipe de desenvolvimento a ter mais autonomia no desenvolvimento de projetos. E uma das reclamações da equipe é o setup local.

Crie um comando para criar um banco de dados PostgreSQL no ambiente do desenvolvedor de uma forma que cumpra os seguintes requisitos:

- O nome do banco de dados deve ser curso_docker
- O usuário de acesso ao banco deve ser docker_usr
- A senha do usuário deve ser docker_pwd
  
Lembrando que a execução em container deve ser transparente pra quem está desenvolvendo. E que aqui você não precisa se preocupar com a perda dos dados do banco e nem nada disso, é apenas para desenvolvimento pontual.
Coloque aqui embaixo o comando que a equipe deve usar pra criar um banco de dados PostgreSQL com esses requisitos.

### Comando a executar:
docker container run -d -p 5432:5432 -e POSTGRES_PASSWORD="docker_pwd" -e POSTGRES_USER=docker_usr -e POSTGRES_DB="curso_docker" --name postgres postgres

# Desafio 02 - Banco de Dados Mysql
## ✨Tarefa:  ✨
Agora que a equipe tem como criar o banco de dados Postgre, crie o comando pra criar o banco de dados MySQL usando os requisitos abaixo:
- O nome do banco de dados deve ser docker_db
- O usuário de acesso ao banco deve ser docker_usr
- A senha do usuário deve ser docker_pwd

Lembrando que a execução em container deve ser transparente pra quem está desenvolvendo. E que aqui você não precisa se preocupar com a perda dos dados do banco e nem nada disso, é apenas para desenvolvimento pontual.

Coloque aqui embaixo o comando que a equipe deve usar pra criar um banco de dados MySQL com esses requisitos:
### Comando a executar:
docker container run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD="P@ssw0rd" -e MYSQL_DATABASE=docker_db -e MYSQL_USER=docker_usr -e MYSQL_PASSWORD="docker_pwd" --name meubanco mysql

# Desafio 03 - Banco de Dados MongoDB
## ✨Tarefa:  ✨
Pra finalizar essa etapa, crie o comando pra criar o banco de dados MongoDB usando os requisitos abaixo:
- O usuário root do banco deve ser mongo_usr
- A senha do usuário root deve ser mongo_pwd

Lembrando que a execução em container deve ser transparente pra quem está desenvolvendo. E que aqui você não precisa se preocupar com a perda dos dados do banco e nem nada disso, é apenas para desenvolvimento pontual.

Coloque aqui embaixo o comando que a equipe deve usar pra criar um banco de dados MongoDB com esses requisitos:
### Comando a executar:
docker run -d --name meubdmongo -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=mongo_usr -e MONGO_INITDB_ROOT_PASSWORD=mongo_pwd mongo
