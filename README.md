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



If all goes well, on Docker Desktop, the ELK services should start running as shown in the example below:



![image](https://github.com/user-attachments/assets/1bf1703d-7f3d-4076-a60c-840aae2f9a16)


After verifying that the ELK network is running, users can verify that each service API is running by using the following commands:


For Elasticsearch, type:

##### http://localhost:9200

An example output is shown below:


![image](https://github.com/user-attachments/assets/494e3936-b38f-4bcf-af55-25f22ef692f6)



Alternately, users can type:


##### curl http://localhost:9200


Note that for some system, users will have to type:


##### curl.exe http://localhost:9200   for the service to work from the IDE terminal. 

For Logstash, type:


##### http://localhost:9600


An example output is shown below:



![image](https://github.com/user-attachments/assets/ea54fc71-977c-4c7e-9830-c7e655ed78cd)


If users prefer to use the IDE command terminal, the command is:


##### curl http://localhost:9600


Note that for some system, users will have to type:
##### curl.exe http://localhost:9600 for the service to work from the IDE terminal. 

For Kibana, type:
##### http://localhost:5601


An example output is shown below:



![image](https://github.com/user-attachments/assets/eb8f60a1-4270-416e-a0ff-dabe2b1d8c47)



If users prefer to use the IDE command terminal, the command is:

##### curl http://localhost:5601


Note that for some system, users will have to type:


##### curl.exe http://localhost:5601 for the service to work from the IDE terminal. 



To further interact with your EKL network, please refer to further suggestions here:

https://github.com/manuelbomi/Data-Engineering--Elasticsearch-Logstash-Kibana-Network-on-Linux-Installation-and-Operationalizing









