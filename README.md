# dev-box-prometheus-graphana-kafka-elastic-logstash-kibana

# 🚀 Elastic stack (ELK) - Prometheus - Graphana - Kafka on Docker for developer box usage 🚀

https://github.com/coding-to-music/dev-box-prometheus-graphana-kafka-elastic-logstash-kibana

From / By Hesapkurdu & Koalay https://github.com/Hesapkurdu

https://github.com/Hesapkurdu/dev-box

## Environment variables:

```java

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
$ docker-compose up
```

By default, the dev box exposes the following ports:

- 5000: Logstash TCP input
- 9200: Elasticsearch HTTP
- 9300: Elasticsearch TCP transport
- 5601: Kibana
- 9090: Prometheus UI
- 3000: Grafana UI (admin:admin)
- 8080: Kafka metrics - <http://localhost:8080/metrics>
