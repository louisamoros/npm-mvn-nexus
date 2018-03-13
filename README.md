# npm-mvn-nexus

How to deploy an angular web application to nexus3 in zip format ?

- launch nexus on docker

`docker run -d -p 8081:8081 --name nexus sonatype/nexus3`

- verify docker nexus is has started

`curl -u admin:admin123 http://localhost:8081/service/metrics/ping`

- package angular web application in zip format

`mvn clean package`

- deploy angular zipped web application to nexus snapshots

`mvn clean deploy`