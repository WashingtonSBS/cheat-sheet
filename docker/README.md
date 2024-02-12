<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" />

<div align="center">
  <h1>📌 DOCKER</h1>
</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" />

<details>
<summary>List images</summary>

## ``List images``

### Usage:
    
    docker images [OPTIONS] [REPOSITORY[:TAG]]
    
### Aliases:
    
    docker image ls, docker image list, docker images
    
### Options:

| Parameter                 | Explanation                                                                                                   |
|:--------------------------|:--------------------------------------------------------------------------------------------------------------|
| -a, --all                 | Show all images (default hides intermediate images)                                                           |
| -f, --filter filter       | Filter output based on conditions provided                                                                    |
| --format string           | Format output using a custom template:                                                                        |
|                           | 'table':            Print output in table format with column headers (default)                                |
|                           | 'table TEMPLATE':   Print output in table format using the given Go template                                  |
|                           | 'json':             Print in JSON format                                                                      |
|                           | 'TEMPLATE':         Print output using the given Go template                                                  |
|                           | Refer to https://docs.docker.com/go/formatting/ for more information about formatting output with templates   |
| --no-trunc                | Don't truncate output                                                                                         |
| -q, --quiet               | Only display container IDs                                                                                    |

### Examples:

> ```bash
> $ docker images -a
> $ docker images --no-trunc --format "table {{.Digest}}\t{{.ID}}\t{{.Repository}}\t{{.Tag}}\t{{.Size}}"
> ```

<br />
</details>

<details>
<summary>List containers</summary>

## ``List containers``

### Usage:
    
    docker container ls [OPTIONS]
    
### Aliases:
    
    docker container ls, docker container list, docker container ps, docker ps
    
### Options:

| Parameter         | Explanation                                                       | State             |
|:------------------|:------------------------------------------------------------------|:------------------|
| -a, --all         | Show all containers (default shows just running)                  | All states        |
| -l, --latest      | Show the latest created container (includes all states)           | All states        |
| -n, --last int    | Show n last created containers (includes all states) (default -1) | All states        |
| -q, --quiet       | Only display container IDs                                        | Just running      |

### Examples:

> ```bash
> $ docker container ls
> $ docker container ls -a
> ```

<br />
</details>

<details>
<summary>Run container</summary>

## ``Run containers``
    
Create and run a new container from an image
    
### Usage:
    
    docker container run [OPTIONS] IMAGE [COMMAND] [ARG...]
    
### Aliases:
    
    docker container run, docker run
    
### Options:

| Parameter                 | Explanation										|
|:--------------------------|:--------------------------------------------------|
| -d, --detach              | Run container in background and print container ID|
| -t, --tty                 | Allocate a pseudo-TTY								|
| -i, --interactive         | Keep STDIN open even if not attached				|
| --rm                      | Automatically remove the container when it exits	|
| --name string             | Assign a name to the container					|
| -p, --publish list        | Publish a containers port(s) to the host			|
| -h, --hostname string     | Container host name								|
| --network network			| Connect a container to a network					|
| -v						| Bind mount a volume								|
   
STDIN - Entrada padrão que o dado, frequentemente texto, está indo para um programa
    
### Examples:

> ```bash
> $ docker container run -dti --rm --name first-hello-world hello-world
> $ docker container run -it -d --rm -p 8080:80 nginx
> $ docker container run -d --hostname my-rabbit --name some-rabbit -p 5672:5672 -p 15672:15672 rabbitmq:3-management
> ```

<br />
</details>

<details>
<summary>Remove containers</summary>

## ``Remove containers``

Remove one or more containers

### Usage:
  
    docker container rm [OPTIONS] CONTAINER [CONTAINER...]
  
### Aliases:
  
    docker container rm, docker container remove, docker rm
  
### Options:

| Parameter                 | Explanation											                      |
|:--------------------------|:------------------------------------------------------|
| -f, --force				        |Force the removal of a running container (uses SIGKILL)|
| -l, --link				        |Remove the specified link								              |
| -v, --volumes				      |Remove anonymous volumes associated with the container	|

### Examples:

> ```bash
> $ docker container rm c98307310146
> $ docker container rm first-hello-world
> ```

</details>
