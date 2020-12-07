# docker-build-env

## Golang

```
docker run --rm \
    -v ~/.ssh:/home/alex_cj96/.ssh \
    -v "$(pwd)":/home/alex_cj96/src \
    alexcj96/golang-build-env:latest \
    bash -c 'eval `ssh-agent -s` ssh-add > /dev/null 2>&1 && go build cmd/example/main.go'
```


## Node

```
docker run --rm \
    -v ~/.ssh:/home/alex_cj96/.ssh \
    -v "$(pwd)":/home/alex_cj96/src \
    alexcj96/node-build-env:latest \
    bash -c 'eval `ssh-agent -s` ssh-add > /dev/null 2>&1 && npm install && npm run build'
```


## Rust

```
docker run --rm \
    -v ~/.ssh:/home/alex_cj96/.ssh \
    -v "$(pwd)":/home/alex_cj96/src \
    alexcj96/rust-build-env:latest \
    bash -c 'eval `ssh-agent -s` ssh-add > /dev/null 2>&1 && cargo build --release'
```
