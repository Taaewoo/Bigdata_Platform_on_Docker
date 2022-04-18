# Bigdata Platform on Docker

## Kafka + Zookeeper
~~~
$ cd kafka
$ docker compose up -d
~~~

## NiFi
~~~
$ cd nifi
$ docker compose up -d
~~~

## NiFi + HDFS
~~~
$ cd nifi
$ docker compose up -f nifi-hdfs-compose.yml -d
~~~

## HDFS namenode HA
~~~
$ cd namenode-ha
$ docker compose up -d
~~~
