
#Find docker slave IP
docker inspect -f '{{.Name}} - {{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' $(docker ps -q)

##RUN on jmeter master##
/opt/apache-jmeter-5.1.1/bin # ./jmeter  -n -t jmeter-docker-compose.jmx -R172.24.0.3