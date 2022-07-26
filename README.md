# dev-box-prometheus-graphana-kafka-elastic-logstash-kibana

# 🚀 Elastic stack (ELK) - Prometheus - Graphana - Kafka on Docker for developer box usage 🚀

https://github.com/coding-to-music/dev-box-prometheus-graphana-kafka-elastic-logstash-kibana

From / By Hesapkurdu & Koalay https://github.com/Hesapkurdu

https://github.com/Hesapkurdu/dev-box

## Environment variables:

```java
cp .env-example .env
```

.env

```java
ELK_VERSION=7.1.1
```

## GitHub

```java
git init
git add .
git remote remove origin
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:coding-to-music/dev-box-prometheus-graphana-kafka-elastic-logstash-kibana.git
git push -u origin main
```

# Elastic stack (ELK) - Prometheus - Graphana - Kafka on Docker for developer box usage

Run the latest version of the [Elastic stack](https://www.elastic.co/elk-stack) with Docker and Docker Compose.

Based on the official Docker images from Elastic:

- [elasticsearch](https://github.com/elastic/elasticsearch-docker)
- [logstash](https://github.com/elastic/logstash-docker)
- [kibana](https://github.com/elastic/kibana-docker)

## Usage

Start the stack using `docker-compose`:

```console
docker-compose up
```

By default, the dev box exposes the following ports:

- 5000: Logstash TCP input
- 9200: Elasticsearch HTTP
- 9300: Elasticsearch TCP transport
- 5601: Kibana
- 9090: Prometheus UI
- 3000: Grafana UI (admin:admin)
- 8080: Kafka metrics - <http://localhost:8080/metrics>

```console
docker-compose down
```

Output

```
Stopping dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_logstash_1      ... done
Stopping dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_kibana_1        ... done
Stopping dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_rabbitmq_1      ... done
Stopping dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_elasticsearch_1 ... done
Stopping dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_redis_1         ... done
```

```
docker-compose -f docker-compose.kafka.yml up
```

Output:

```
WARNING: Some services (prometheus) use the 'deploy' key, which will be ignored. Compose does not support 'deploy' configuration - use `docker stack deploy` to deploy to a swarm.

WARNING: Found orphan containers (dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_redis_1, dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_elasticsearch_1, dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_rabbitmq_1, dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_logstash_1, dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_kibana_1) for this project. If you removed or renamed this service in your compose file, you can run this command with the --remove-orphans flag to clean it up.

dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_kafka_1 is up-to-date
dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_prometheus_1 is up-to-date

Starting dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_kafka-jmx-exporter_1 ...
Starting dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_kafka-jmx-exporter_1 ... error
Starting dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_graf-db_1            ... done

ERROR: for dev-box-prometheus-graphana-kafka-elastic-logstash-kibana_kafka-jmx-exporter_1  Cannot start service kafka-jmx-exporter: failed to create shim task: OCI runtime create failed: runc create failed: unable to start container process: exec: "/opt/entrypoint.sh": permission denied: unknown

ERROR: for kafka-jmx-exporter  Cannot start service kafka-jmx-exporter: failed to create shim task: OCI runtime create failed: runc create failed: unable to start container process: exec: "/opt/entrypoint.sh": permission denied: unknown
ERROR: Encountered errors while bringing up the project.
```
