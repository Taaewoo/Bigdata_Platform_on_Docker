# Airflow 클러스터 구성하기

### Airflow
- Airflow Web : [http:localhost:18080](http:localhost:18080)
~~~
$ cd airflow
$ mkdir ./dags ./logs ./plugins
$ echo -e "AIRFLOW_UID=$(id -u)\nAIRFLOW_GID=0" > .env
$ docker-compose up airflow-init
$ docker compose up -d
~~~
