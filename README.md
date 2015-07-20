# Hadoop cluster on Virtual box with Docker

### Mac OSx

#### Prerequisites checklist

*   [Virtual box](https://www.virtualbox.org/)
*   [Boot2docker](http://boot2docker.io/)
*   [Docker-Compose](https://docs.docker.com/compose/install/)

#### Setup:

```sh
1. mkdir hadoopUpAndRunning
2. cd hadoopUpAndRunning
3. create docker-compose.yml file
4. copy content from README page of [This docker image](https://registry.hub.docker.com/u/badele/debian-hadoop/)
5. boot2docker init
6. boot2docker up
```
#### Init HDFS

```sh
docker-compose run namenode hdfs namenode -format

```

#### Start hadoop cluster

```sh
docker-compose up -d

```

#### Check port numbers and ip address

```sh
$ docker ps
$ boot2docker ip

```

#### Access hadoop web-ui:
```sh
http://{boot2docker ip-address}:{port number of namenode}/
sample: http://192.168.59.103:50070

```


