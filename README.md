## compiler 

mvnd clean package -DskipTests  -T 10 -Dcheckstyle.skip -Drat.skip

##  edit host file
   127.0.0.1 peer-1-server.com
   127.0.0.1 peer-2-server.com
   127.0.0.1 peer-3-server.com
   
## run eureka server 
    java -jar -Dspring.profiles.active=peer-1 target/eureka-server-0.0.1-SNAPSHOT.jar
    java -jar -Dspring.profiles.active=peer-2 target/eureka-server-0.0.1-SNAPSHOT.jar
    java -jar -Dspring.profiles.active=peer-3 target/eureka-server-0.0.1-SNAPSHOT.jar
