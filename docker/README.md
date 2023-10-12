<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" />

<div align="center">
  <h1>📌 DOCKER</h1>
</div>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" />

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

### Example:

> ```bash
> $ docker images --no-trunc --format "table {{.Digest}}\t{{.ID}}\t{{.Repository}}\t{{.Tag}}\t{{.Size}}"
> ```

<br />

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

### Example:

> 
> ```bash
> $ docker container ls -a
> ```
> 
