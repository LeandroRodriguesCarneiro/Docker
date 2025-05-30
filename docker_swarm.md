`docker swarm init`  Para iniciar um swarm e maquina virar um node a primeira maquina vira um manager
  - `docker swarm init --advertise-addr {ip-node}`  Para iniciar um swarm
- `docker node ls`  Para listar os nodes
- `docker swarm join --token {token} {ip-node}:{porta}`  Para adicionar um node worker
- `docker swarm join-token manager`  Para recuperar o token do manager
- `docker service create --name {name} -p {porta-swarm}:{porta-host} {imagem}`  Para criar um servico
- `docker service create --name {name} --replicas {n-replicas} -p {porta-swarm}:{porta-host} {imagem}`  Para criar um servico
- `docker service ls`  Para listar os serviços apenas o manager
- `docker service rm {nome}`  Para listar os serviços apenas o manager
- `docker service rm {nome}`  Para listar os serviços apenas o manager
