docker service create --name registry --publish 5000:5000 registry:2
docker build -t 127.0.0.1:5000/prometheus2 .
docker push 127.0.0.1:5000/prometheus2
docker stack deploy -c compose.yml prometheus