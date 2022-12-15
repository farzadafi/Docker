<h1>Docker Cheat Sheet</h1>

<h2>Containers</h2>

<h4>_Start a new Container from an Image_</h4>
    `docker run IMAGE` <br>
    `docker run postgres`

<h4>Assign a name to container</h4>
`docker run --name CONTAINER_NAME IMAGE` <br>
`docker run --name web postgres`


<h4>_Map a port to container_</h4>
`docker run -p HOSTPORT:CONTAINERPORT IMAGE` <br>
`docker run -p 8680:80 postgres`


<h4>Map all ports to container</h4>
`docker run -P IMAGE` <br>
`docker run -P postgres`

<h4>Start container in background</h4>
`docker run -d IMAGE` <br>
`docker run -d postgres`

<h4>Assign a hostname to container</h4>
`docker run --hostname HOSTNAME IMAGE` <br>
`docker run --hostname myhost postgres`

<h4>Show a list of running container</h4>
`docker ps`

<h4>Show a list of all containers</h4>
`docker ps -a`

<h4>Delete a container</h4>
`docker rm CONTAINER_NAME` <br>
`docker rm web`

<h4>Delete a running container</h4>
`docker rm -f CONTAINER_NAME` <br>
`docker rm -f postgres`

<h4>Delete stopped container</h4>
`docker container prune`

<h4>Stop a running container</h4>
`docker stop CONTAINER_NAME` <br>
`docker stop postgres`

<h4>Start a stopped container</h4>
`docker start CONTAINER_NAME` <br>
`docker start postgres`

<h4>Copy file from container to host</h4>
`docker cp CONTAINER_NAME:SOURCE TARGET` <br>
`docker cp postgres:/index.html index.html`

<h4>Copy file from the host to container</h4>
`docker cp TARGET CONTAINER_NAME:HOST` <br>
`docker cp index.html postgres:/index.html`

<h4>Renaming a Container</h4>
`docker stop old_name new_name` <br>
`docker rename postgres postgresNew`

<h4>Restarting a container</h4>
`docker stop CONTAINER_NAME` <br>
`docker restart postgres`

<h4>Pausing a container</h4>
`docker pause CONTAINER_NAME`
`docker pause postgres`

<h4>Start a shell inside a running container</h4>
`docker exec -it CONTAINER_NAME SHELL_NAME` <br>
`docker exec -it postgres bash`

