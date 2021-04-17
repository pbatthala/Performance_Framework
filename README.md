# Performance_Framework
## Preconfiguration(optional but preferable)
---------------
You need this items for performance framework
- Install docker [Docker install website](https://docs.docker.com/engine/install/)
- Install WSL 2 (optional)[WSL2 install guide][2]
- Install Java (8 version or higher) 
## Installing
---------------
For installing and building framework you need to:
1. Download repository: [here][3]
2. For quick install navigate to repository dir and choose framework load tool(jmeter or gatling).
 ```docker-compose up -d```
3. If you want to install separate container
```docker compose up -d elasticsearch
  docker compose up -d kibana 
  docker compose up -d logstash
  docker compose up -d filebeat
  docker compose up -d metricbeat
  docker compose up -d portainer
  docker compose up -d web
  docker compose up -d jenkins
  ```
If you want only build container use this command.
```
docker-compose build -d
```
After building and creating containers services have such adresses and ports:
- Jenkins: localhost:8080
- Kibana: localhost:5601
- Portainer: localhost:9000
- Flask app: localhost:5000
4. Navigate to jenkins(Login: admin, Password: admin).
If you want to use github(by default basic scipts download from github repository) add credentials by this path **options->credentials**

[2]: https://docs.microsoft.com/en-us/windows/wsl/install-win10
[3]: https://github.com/youketero/Performance_Framework