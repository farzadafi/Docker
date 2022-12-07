<h1>simple hello docker app</h1>

<p>
After create this module or clone this repo enters:
</p>

<code>sudo docker build -t helloDocker .</code>

<p>
with this command create an image with name helloDocker, and you can see it with command:
</p>

<code>sudo docker images</code>

<p>
finally you can start a new container from helloDocker image with command:
</p>

<code>sudo docker run -it -p 8080:8080 helloDocker</code>

<p>
and then Please call this url:
</p>

[hello docker 😍](http://localhost:8080/hello)