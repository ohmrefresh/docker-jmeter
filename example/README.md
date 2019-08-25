
#Find docker slave IP
docker inspect -f '{{.Name}} - {{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' $(docker ps -q)|grep slave|awk '{print $3}'| xargs | sed -e 's/ /,/g'

##RUN on jmeter master##
/opt/apache-jmeter-5.1.1/bin # ./jmeter -Gfile_csv=/home/file.csv -n -t /home/demo.jmx -Dserver.rmi.ssl.disable=true -R192.168.128.3,192.168.128.4