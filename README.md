# virtuoso-docker

Docker build for virtuoso-opensource https://github.com/openlink/virtuoso-opensource

Can be found on the docker hub https://hub.docker.com/r/opendataservices/virtuoso/

## Usage

Either build it `docker build -t opendataservices/virtuoso .` or pull from docker hub `docker pull opendataservices/virtuoso`.
Then run it:

```
docker run -p 127.0.0.1:8890:8890 --name=virtuoso -v /usr/local/var/lib/virtuoso/db opendataservices/virtuoso 
```

You can then access it from another container using --link, e.g.

```
docker run --link virtuoso:virtuoso {other_image_name}
```
