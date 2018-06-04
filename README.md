

docker network create -d overlay --attachable network-logging

docker stack deploy -c 1-elasticsearch-docker-compose.yml stack-logging

docker stack deploy -c 2-kibana-docker-compose.yml stack-logging

docker stack deploy -c 3-tools-docker-compose.yml stack-logging

docker stack deploy -c 4-filebeat-docker-compose.yml stack-logging


se rendre dans kibana et créer l'index pattern

filebeat-*