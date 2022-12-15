<h1>Docker Cheat Sheet</h1>

<h2>Containers</h2>

<h4>Start a new Container from an Image</h4>
<code>docker run IMAGE</code> <br>
<code>docker run postgres</code>

<h4>Assign a name to container</h4>
<code>docker run --name CONTAINER_NAME IMAGE</code> <br>
<code>docker run --name web postgres</code>


<h4>Map a port to container</h4>
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
<hr>

<h2>Images</h2>

<h4>Download an Image</h4>
<code>docker pull IMAGE[:TAG] </code> <br>
<code>docker pull postgres:latest</code>

<h4>See list of all images</h4>
<code>docker images </code>

<h4>Run the docker image</h4>
<code>docker run IMAGE_NAME </code> <br>
<code>docker run postgres</code>

<h4>Upload an image to a repository</h4>
<code>docker push IMAGE_NAME:TAG </code> <br>
<code>docker push postgres:latest</code>

<h4>Login to a Registry</h4>
<code>docker logindocker login localhost:8080 </code>

<h4>Delete an image</h4>
<code>docker rmi IMAGE_NAME </code> <br>
<code>docker rmi postgres</code>

<h4>Delete all unused images</h4>
<code>docker image prune -a </code>

<h4>Build an image form Dockerfile</h4>
<code>docker build -t IMAGE_NAME DIRECTORY </code> <br>
<code>docker build -t postgres .</code>

<h4>Save an image to .tar file</h4>
<code>docker save IMAGE_NAME > File </code> <br>
<code>docker save postgres > postgres.tar</code>

<h4>Load an image from .tar file</h4>
<code>docker load -i TAR_FILE_NAME </code> <br>
<code>docker load -i postgres.tar</code>
<hr>

<h2>Logs and Stats</h2>

<h4>Show the logs of container</h4>
<code>docker logs CONTAINER_NAME </code> <br>
<code>docker logs postgres</code>

<h4>Show a stats of running container</h4>
<code>docker stats [container_Id]</code>

<h4>Show processes of container</h4>
<code>docker top CONTAINER_NAME </code> <br>
<code>docker top postgres</code>

<h4>Show detailed information</h4>
<code>docker inspect CONTAINER_NAME </code> <br>
<code>docker inspect postgres </code>
<hr>

