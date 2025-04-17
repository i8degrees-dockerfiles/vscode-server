
# vscode-server

Visual Studio Code IDE server

## usage

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
```

## reference documents

[0]:
[90]:
[100]:
[110]:

