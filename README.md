# Bigdata Platform on Docker

## Git Clone
~~~
$ git clone https://github.com/Taaewoo/Bigdata_Platform_on_Docker.git
~~~

## Bigdata Components

### Kafka + Zookeeper
~~~
$ cd kafka
$ docker compose up -d
~~~

### Airflow
~~~
$ cd airflow
$ mkdir ./dags ./logs ./plugins
$ echo -e "AIRFLOW_UID=$(id -u)\nAIRFLOW_GID=0" > .env
$ docker-compose up airflow-init
$ docker compose up -d
~~~
Airflow Web : (http:localhost:18080)

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
