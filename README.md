# Bigdata Platform on Docker

## Git Clone
~~~
$ git clone https://github.com/Taaewoo/Bigdata_Platform_on_Docker.git
~~~

## Bigdata Components

### Kafka + Zookeeper
- Kafka Manager Web : [http:localhost:9000](http:localhost:9000)
~~~
$ cd kafka
$ docker compose up -d
~~~

### Airflow
- Airflow Web : [http:localhost:18080](http:localhost:18080)
~~~
$ cd airflow
$ mkdir ./dags ./logs ./plugins
$ echo -e "AIRFLOW_UID=$(id -u)\nAIRFLOW_GID=0" > .env
$ docker-compose up airflow-init
$ docker compose up -d
~~~


### NiFi + Zookeeper
- NiFi Web : [http:localhost:6980](http:localhost:6980)
~~~
$ cd nifi
$ docker compose up -d
~~~

### NiFi + Zookeeper + HDFS
- NiFi Web : [http:localhost:6980](http:localhost:6980)
~~~
$ cd nifi
$ docker compose up -f nifi-hdfs-compose.yml -d
~~~

### Spark + HDFS
~~~
$ cd spark
$ mkdir -p data/namenode
$ mkdir -p data/datanode
~~~

### HDFS namenode HA
~~~
$ cd namenode-ha
$ docker compose up -d
~~~
