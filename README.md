<h1>Docker Cheat Sheet</h1>

<h2>Containers</h2>

<h4>_Start a new Container from an Image_</h4>
<code>docker run IMAGE</code> <br>
<code>docker run postgres</code>

<h4>Assign a name to container</h4>
<code>docker run --name CONTAINER_NAME IMAGE</code> <br>
<code>docker run --name web postgres</code>


<h4>_Map a port to container_</h4>
<code>docker run -p HOSTPORT:CONTAINERPORT IMAGE</code> <br>
<code>docker run -p 8680:80 postgres</code>


<h4>Map all ports to container</h4>
<code>docker run -P IMAGE</code> <br>
<code>docker run -P postgres</code>

<h4>Start container in background</h4>
<code>docker run -d IMAGE</code> <br>
<code>docker run -d postgres</code>

<h4>Assign a hostname to container</h4>
<code>docker run --hostname HOSTNAME IMAGE</code> <br>
<code>docker run --hostname myhost postgres</code>

<h4>Show a list of running container</h4>
<code>docker ps</code>

<h4>Show a list of all containers</h4>
<code>docker ps -a</code>

<h4>Delete a container</h4>
<code>docker rm CONTAINER_NAME</code> <br>
<code>docker rm web</code>

<h4>Delete a running container</h4>
<code>docker rm -f CONTAINER_NAME</code> <br>
<code>docker rm -f postgres</code>

<h4>Delete stopped container</h4>
<code>docker container prune</code>

<h4>Stop a running container</h4>
<code>docker stop CONTAINER_NAME</code> <br>
<code>docker stop postgres</code>

<h4>Start a stopped container</h4>
<code>docker start CONTAINER_NAME</code> <br>
<code>docker start postgres</code>

<h4>Copy file from container to host</h4>
<code>docker cp CONTAINER_NAME:SOURCE TARGET</code> <br>
<code>docker cp postgres:/index.html index.html</code>

<h4>Copy file from the host to container</h4>
<code>docker cp TARGET CONTAINER_NAME:HOST</code> <br>
<code>docker cp index.html postgres:/index.html</code>

<h4>Renaming a Container</h4>
<code>docker stop old_name new_name</code> <br>
<code>docker rename postgres postgresNew</code>

<h4>Restarting a container</h4>
<code>docker stop CONTAINER_NAME</code> <br>
<code>docker restart postgres</code>

<h4>Pausing a container</h4>
`docker pause CONTAINER_NAME</code>
<code>docker pause postgres</code>

<h4>Start a shell inside a running container</h4>
<code>docker exec -it CONTAINER_NAME SHELL_NAME</code> <br>
<code>docker exec -it postgres bash</code>

