FROM ohmrefresh/docker-jmeter:latest

EXPOSE 1099 50000
#GC_ALGO="-XX:+UseG1GC -XX:MaxGCPauseMillis=100 -XX:G1ReservePercent=20"
#HEAP="-Xms1g -Xmx1g -XX:MaxMetaspaceSize=256m"
#JVM_ARGS=""

ENTRYPOINT $JMETER_HOME/bin/jmeter-server \
                        -Dserver.rmi.localport=50000 \
                        -Dserver_port=1099 \
                        -Dserver.rmi.ssl.disable=true