FROM openjdk:11-jre-slim
WORKDIR usr/src
ENV MONGO_URI mongodb://mongodbservice:27017/movie_db
ENV MONGO_DB_NAME movie_db
ADD ./target/UserMovieService-0.0.1-SNAPSHOT.jar /usr/src/UserMovieService-0.0.1-SNAPSHOT.jar
ENTRYPOINT ["java","-Dspring.data.mongodb.uri=mongodb://mongodbservice:27017/movie_db","-jar","UserMovieService-0.0.1-SNAPSHOT.jar"]
