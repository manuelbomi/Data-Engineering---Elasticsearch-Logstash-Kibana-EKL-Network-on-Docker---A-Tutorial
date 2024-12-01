# Data-Engineering---Elasticsearch-Logstash-Kibana-EKL-Network-on-Docker---A-Tutorial

We present a docker-compose.yml file through which the Elasticsearch-Logstash-Kibana (EKL) network can be installed on Windows operating system via WSL.

Full background and details regarding the use of the EKL network for data engineering application can be obtained here:   

https://github.com/manuelbomi/Data-Engineering--Elasticsearch-Logstash-Kibana-Network-on-Linux-Installation-and-Operationalizing

Users can download docker-compose.yml file from this Github page. 

To verify after downloading the docker-compose.yml, create a file on your IDE of choice (e,g. Visual Studio Code), add the docker-compose.yml document to the file and run <ins> docker-compose up </ins>. Ensure the Docker Desktop is running before you run <ins> docker-compose up </ins>. 

If running for the first time, Docker will first pull Elasticsearch, Logstash and Kibana from their respective home pages and integrate them with the local Docker Desktop. After Docker have pulled the ELK network, users can start Elasticsearch, Logstash and Kibana by typing the following commands on the IDE terminal. 
#### docker start elasticsearch
#### docker start logstash
#### docker start kibana

An example (using VSCode) is shown below:

![image](https://github.com/user-attachments/assets/435cce98-3f3e-4c95-8877-1d661ab427e6)

