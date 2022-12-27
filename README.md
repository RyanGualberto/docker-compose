### Docker Commands

- Pull Image

```
    docker pull [image] || [image]:[version]
```

- Create and Run a container

```
    docker run [flags] -p [port_local]:[port_container] [image] || docker run [flags] -d -p [port_local]:[port_container] [image] (to run on background)
```

- Stop a container

```
    docker stop [container]
```

- Remove a container

```
    docker rm [container] || [container_id]
```

- list running container

```
    docker ps
```

- list created container

```
    docker ps -a
```

- list all images installeds

```
    docker images
```

### How to use a docker compose

- First Step

    create a file with name "docker-compose.yml"

- Second Step

On "docker-compose.yml" type

```
    version: "3.4" (latest version)
```

- Third step
List and config your containers

```
    Services: 
        [service_name]: 
            container_name: [container_name]
            image: [image_required]
            ports: 
              - [port_local]:[port_container]
            environment:
              - [env_variable]=[env_value]
            build: . (local of docker compose) 
```


