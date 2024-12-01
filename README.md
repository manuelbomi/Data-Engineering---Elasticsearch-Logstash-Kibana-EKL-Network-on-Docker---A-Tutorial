# Data-Engineering---Elasticsearch-Logstash-Kibana-EKL-Network-on-Docker---A-Tutorial

We present a docker-compose.yml file through which the Elasticsearch-Logstash-Kibana (EKL) network can be installed on Windows operating system via WSL.

Full background and details regarding the use of the EKL network for data engineering application can be obtained here:   

https://github.com/manuelbomi/Data-Engineering--Elasticsearch-Logstash-Kibana-Network-on-Linux-Installation-and-Operationalizing

The .yml file is presented below. Users can also download it from this Github page. 


version: '3.7'

services:
  elasticsearch:
    image: docker.elastic.co/elasticsearch/elasticsearch:8.10.3
    container_name: elasticsearch
    environment:
      - discovery.type=single-node
      - xpack.security.enabled=false 
      #- ES_JAVA_OPTS=-Xheap:512m -Xms:512m
    ulimits:
      memlock:
        soft: -1
        hard: -1
    #volumes:
      #- elasticsearch-data:/usr/share/elasticsearch/data
    ports:
      - 9200:9200
      - 9300:9300

  logstash:
    image: docker.elastic.co/logstash/logstash:8.10.3
    container_name: logstash
    #volumes:
      #- ./logstash.conf:/usr/share/logstash/pipeline/logstash.conf
    depends_on:
      - elasticsearch
    ports:
      - 5044:5044
      - 5000:5000/tcp
      - 5000:5000/udp
      - 9600:9600
    expose:
      - 5044
    #networks:
    #default:
    #name: elasticsearch_default
    #external: true
    links:
    - elasticsearch

  kibana:
    image: docker.elastic.co/kibana/kibana:8.10.3
    container_name: kibana
    depends_on:
      - elasticsearch
    ports:
      - 5601:5601



#volumes:
  #elasticsearch-data: {}









To verify after downloading the docker-compose.yml, create a file on your IDE (e,g. Visual Studio Code) of choice, add the docker-compose.yml document to the file and run <ins> docker-compose up </ins>. Ensure the Docker Desktop is running before you run <ins> docker-compose up </ins>. 

If running for the first time, Docker will first pull Elasticsearch, Logstash and Kibana from their respective home pages and integrate them with the local Docker Desktop. After Docker have pulled the ELK network, users can start Elasticsearch, Logstash and Kibana by typing the following commands on the IDE terminal. 
#### docker start elasticsearch
#### docker start logstash
#### docker start kibana

An example (using VSCode) is shown below:
