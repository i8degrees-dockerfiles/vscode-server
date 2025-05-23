
# vscode-server

Visual Studio Code IDE server uplink.

- [docker.fs1.home: code tunnel](http://docker.fs1.home:8010)

## usage

- [Remote Code Tunnels][0]
- web UI for vscode instance

### bootstrap

```sh
git clone "https://github.com/i8degrees-dockerfiles/vscode-server.git \
    vscode-server.git"
cd "vscode-server.git" || exit 2
```

```sh
# initial image compilation; see build.sh
docker compose build
# external network declaration
docker network create proxy
```

### service control

#### service start

```sh
docker compose up -d
```

##### service start from scratch

```sh
docker compose up -d --force-recreate
```

##### service query

```sh
docker compose ps
```

#### service stop

```sh
docker compose down
#docker compose down --remove-orphans
```

#### service logs

```sh
docker compose logs
docker compose logs --since=5m
docker compose logs --since=24h -f
```

#### debugging

##### attach to shell

```sh
docker exec -it vscode-server-1 bash
#docker exec -it vscode-server-1 sh
```

##### push to hub

```sh
docker compose push
```

##### pull from hub

```sh
docker compose pull
```

## reference documents

[0]: https://code.visualstudio.com/docs/remote/tunnels
[10]:
[90]:
[100]:
[110]:

