FROM openjdk:11-jdk-slim
COPY twitter-producer/target/twitter-producer-1.0-SNAPSHOT.jar app.jar
EXPOSE 8080
ARG TWITTER_CONSUMER_KEY
ARG TWITTER_CONSUMER_SECRET
ARG TWITTER_ACCESS_TOKEN_SECRET
ARG TWITTER_ACCESS_TOKEN

ENV TWITTER_CONSUMER_KEY=${TWITTER_CONSUMER_KEY}
ENV TWITTER_CONSUMER_SECRET=${TWITTER_CONSUMER_SECRET}
ENV TWITTER_ACCESS_TOKEN_SECRET=${TWITTER_ACCESS_TOKEN_SECRET}
ENV TWITTER_ACCESS_TOKEN=${TWITTER_ACCESS_TOKEN}

ENTRYPOINT ["java","-jar","/app.jar","kafka:9092" ,"df", "elasticsearch7", "9300", "trump", "biden"]



