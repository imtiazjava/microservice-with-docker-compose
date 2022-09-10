FROM openjdk:11-jre-slim
WORKDIR usr/src
EXPOSE 8085
ENV MYSQL_URL jdbc:mysql://mysqlservice:3306/registered_users?useSSL=false&createDatabaseIfNotExist=true&allowPublicKeyRetrieval=true
ADD ./target/UserAuthenticationService-0.0.1-SNAPSHOT.jar /usr/src/UserAuthenticationService-0.0.1-SNAPSHOT.jar
ENTRYPOINT ["java","-Dspring.datasource.url=jdbc:mysql://mysqlservice:3306/registered_users?useSSL=false&createDatabaseIfNotExist=true&allowPublicKeyRetrieval=true","-jar","UserAuthenticationService-0.0.1-SNAPSHOT.jar"]