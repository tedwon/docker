## Docker images to test Infinispan/Spark integration

### Building the image

To create the image, run the provided ```build.sh``` script.

### Launching:

Launch a container with spark master, spark worker and infinispan server:

```
docker run --name master -ti gustavonalle/infinispan-spark
```

Launch one or more worker containers, that holds infinispan server and a spark worker:

```
docker run -ti --link master:master  gustavonalle/infinispan-spark
```

To check the master ip address, run: ```docker inspect master```

```
sudo route -n add 172.17.0.0/16 `docker-machine ip default`
```

The admin UI will listen at ```http://master-ip:9080```

http://172.17.0.3:9080/
