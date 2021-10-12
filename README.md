# Confluent Platform + ELK

control-center + broker + zookeeper + logstash + elasticsearch + kibana

Source Kafka : https://github.com/confluentinc/cp-all-in-one

Source ELK : https://github.com/deviantony/docker-elk

## Pre-requis

- Ajouter **broker** a la premiere ligne de /etc/hosts

      $ sudo gedit /etc/hosts
      127.0.0.1	localhost broker
- Modifier aussi les Run Configurations (localhost:9092 -> **broker**:9092)

## Infos utiles

- Control Center : http://localhost:9021
- Elasticsearch : http://localhost:9200
    - user:password : elastic:changeme
    - Lister les indexes : http://localhost:9200/_cat/indices
- Kibana (elastic:changeme): http://localhost:5601
  - user:password : elastic:changeme

## Lancement

    docker-compose up -d

## Arret

    docker-compose down
