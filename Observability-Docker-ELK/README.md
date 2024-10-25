# Observability with Docker Compose and ELK
Setting up an ELK stack (Elasticsearch, Logstash, and Kibana) using Docker containers is a straightforward way to quickly deploy centralized logging for your application. 

1. Elasticsearch: Handles storage, indexing, and querying of log data.2.
2. Logstash: Processes and transforms data before sending it to Elasticsearch.
3. Kibana: Provides a UI to visualize, search, and analyze the data.

### Step 1: Install Docker and Docker Compose
Make sure Docker and Docker Compose are installed on your system.(Installation)

### Step 2: Create a Docker Compose File
Create a **docker-compose.yml** file to define the configuration for the ELK stack.

### Step 3: Configure Logstash
Create a **logstash.conf** file to configure Logstash input, filter, and output. This is where you can define data ingestion configurations.

### Step 4: Start the ELK Stack
Run the following command to start all containers:
  ```
  docker-compose up -d
  ```
### Step 5: Access ELK
- Kibana: http://localhost:5601
- Logstash: http://localhost:5601
- Elasticsearch: http://localhost:9200

### Step 6: Configure Beats (Optional)
If you want to ingest logs from a file or other sources, you can configure Filebeat, Metricbeat, or another beat to send data to Logstash. 
- Install the Beat on your host machine and set the output to Logstash at localhost:5044.

#### ELK Stack Commands
- View logs: docker logs elasticsearch
- Stop containers: docker-compose down
- Access Elasticsearch: curl http://localhost:9200
