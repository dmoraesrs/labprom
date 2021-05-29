# COmando
HOSTNAME=$(hostname) docker stack deploy -c docker-stack.yml prom
docker stack ps prom
docker service ls
docker service create --name my_web --replicas 1 --publish published=8090,target=80 nginx
docker service scale my_web=1
