# criar image
docker build -t marcelobohn/rails-docker:0.0.1 .

# mais listar a imagem criada
docker images

# rodar e deixar terminal 'pendurado'
docker run -it -p 3000:3000 marcelobohn/rails-docker:0.0.1

# rodar e libera o console
docker run -d -p 3000:3000 marcelobohn/rails-docker:0.0.1
# para desligar roda os e pega o id o container
docker ps
# parar o container
docker stop $id_rondando


pode ser necessário matar o processo manualmente

# lista processos
netstat -vanp tcp | grep 3000
# ou
lsof -i tcp:3000

#com o pid do processo
kill $pid
