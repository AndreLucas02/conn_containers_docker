criar um network no docker chamado -> flasknetwork 

entrar na pasta mysql e usar o comando ->  docker build -t mysqlnetworkapi .

entrar na pasta flask e usar o comando ->  docker build -t flasknetworkapi .

rodar os containers
flask -> docker run -d -p 5000:5000 --name flask_api_container --rm --network flasknetwork flasknetworkapi

mysql -> docker run -d -p 3306:3306 --name mysql_api_container --rm --network flasknetwork -e MYSQL_ALLOW_EMPTY_PASSWORD=true mysqlnetworkapi

baixe o postman para os testes, usando o link que estão no method get e post em flask/app.py

use o mysqlworkbanch para visualar os dados do banco. 
