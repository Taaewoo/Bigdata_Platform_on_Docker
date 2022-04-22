# Bigdata Platform on Docker

## Git Clone
~~~
$ git clone https://github.com/Taaewoo/Bigdata_Platform_on_Docker.git
~~~

### Kafka + Zookeeper
~~~
$ cd kafka
$ docker compose up -d
~~~

### NiFi + Zookeeper
~~~
$ cd nifi
$ docker compose up -d
~~~

### NiFi + Zookeeper + HDFS
~~~
$ cd nifi
$ docker compose up -f nifi-hdfs-compose.yml -d
~~~

### HDFS namenode HA
~~~
$ cd namenode-ha
$ docker compose up -d
~~~
