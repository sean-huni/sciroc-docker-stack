# Rock Paper Scissors (Game)

This is a Spring-Cloud Portfolio of projects that are closely related together to deliver a single gaming platform.

## Full-Stack

### Cloud Servers/Swarm:
1. [node-1 (178.128.248.16) - Manager](178.128.248.16)
2. [node-2 (178.128.254.229) - Worker](178.128.254.229)
3. [node-3 (178.128.241.236) - Worker](178.128.241.236)
4. [node-4 (178.128.245.141) - Worker](178.128.245.141)

[Click here to visualise the Swarm](http://178.128.248.16:9000/#/swarm/visualizer)

### Dev-Stack
- Docker-Stacks
- Docker-Compose
- Docker-Swarm
- Neo4j
- RabbitMQ
- Zipkin Server
- Spring Boot
- Spring Actuator
- Spring Boot Admin
- Spring Cloud (Netflix):
    - Ribbon (Client-Side Load-Balancer)
    - Hystrix
    - Hystrix Dashboard
    - Turbine
    - Config (Server & Client)
    - Zuul (API-Gateway)
    - Feign/OpenFeign
    - Eureka (Server & Service Discovery)
    - Sleuth
    - Zipkin
- Web:
    - Spring MVC
    - Thymeleaf
    - Bootstrap
    - JQuery
    - DataTables (https://datatables.net/)

### Microservices API Documentation

URL: 178.128.248.16:\<port>

- [Swagger-2](http://178.128.248.16:8004/swagger-2/)

### Microservices Ports:

- RabbitMQ (Server) ------  [15672](http://178.128.248.16:15672)
- Portainer (Server) -----  [9000](http://178.128.248.16:9000)
- Neo4j (DB-Server) ------  [7474](http://178.128.248.16:7474)
- Zipkin (Server) --------  [9411](http://178.128.248.16:9411)
- Sciroc-Web (MVC) -------  [8000](http://178.128.248.16:8000)
- Eureka -----------------  [8001](http://178.128.248.16:8001)
- Config (Server) --------  [8002](http://178.128.248.16:8002)
- Leader-Data ------------  [8003](http://178.128.248.16:8003)
- Leaderboard ------------  [8004](http://178.128.248.16:8004)
- Zuul (API-Gateway) -----  [8005](http://178.128.248.16:8005)
- Game -------------------  [8006](http://178.128.248.16:8006)
- Turbine ----------------  [8007](http://178.128.248.16:8007/hystrix)
    - Copy/Paste the URL below into the Turbine-Dashboard:
        
        http://178.128.248.16:8004/actuator/hystrix.stream
    
### Repository Portfolio (Public):

1.  [Config Repo](https://bitbucket.org/sean-huni/config)
2.  [Config (Server)](https://bitbucket.org/sean-huni/config-server)
3.  [Sciroc-Web (MVC)](https://bitbucket.org/sean-huni/sciroc)
4.  [Eureka](https://bitbucket.org/sean-huni/eureka)
5.  [Leader-Data](https://bitbucket.org/sean-huni/leader-data)
6.  [Leaderboard](https://bitbucket.org/sean-huni/leaderboard)
7.  [Zuul (API-Gateway)](https://bitbucket.org/sean-huni/zuul)
8.  [Game](https://bitbucket.org/sean-huni/game)
9.  [Turbine](https://bitbucket.org/sean-huni/turbine)

# Rock-Paper-Scissors Game - Docker Stack

To deploy the docker stack run the following command:

  **`git clone https://github.com/sean-huni/sciroc-docker-stack.git`**
  
  **`cd sciroc-docker-stack`**
  
  **`./pull-img.sh`**
  
  **`docker stack deploy -c docker-compose.yml rps`**
  
  **`docker service ls`**
  
  **`docker service ps rps_leader-data`**
  
  **`docker service logs rps_leaderboard --tail 10 -f`**
  
  **`docker service scale rps_game=2`**

**Note: links to the bitbucket repo have been be listed Above**
