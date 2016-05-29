# DockerFiles

## myWildFlyContainer
It builds an image with a wildfly listening to 0.0.0.0 and creates an administration user. It also attach a directory (<deployment_dir> in the next commands) to deploy applications from the host to the container.

### How to run it
```bash
cd myWildFlyContainer
docker build -t albpal/mywildfly .
docker run -p 8080:8080 -p 9990:9990 -d -v <deployment_dir>:/opt/jboss/wildfly/standalone/deployments/:rw albpal/mywildfly
docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                                            NAMES
f316c63a1db3        albpal/mywildfly    "/opt/jboss/wildfly/b"   3 seconds ago       Up 2 seconds        0.0.0.0:8080->8080/tcp, 0.0.0.0:9990->9990/tcp   prickly_euler
```
