## Desenvolvimento

Inicializar mqtt on docker via compose:

```sh
docker-compose -d -p mqtt5 up
```

Abrir uma shell dentro do container de mqtt:

```sh
#List containers
docker ps
#opens a shell inside a container
docker exec -it <container-id> sh
```

> Note: `/ #` no terminal.

Adicionar um user para o mqtt:

```sh
#Adicionar user mqtt
mosquitto_passwd -c /mosquitto/config/pwfile mqtt
#Enter password promp

#Fix file owner
chown root /mosquitto/config/pwfile
#Fix permission
chmod 0700 /mosquitto/config/pwfile
exit
```

Reniciar o container:

```sh
#Restarts docker container
docker restart <container-id>
```
