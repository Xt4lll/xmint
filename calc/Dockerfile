FROM ubuntu:latest

RUN apt-get update && apt-get install -y \
openjdk-11-jre \
x11-apps \
xauth \
&& rm -rf /var/lib/lists/*

ENV DISPLAY=host.docker.internal:0

WORKDIR /app

COPY calc.jar /app/calc.jar

CMD ["java", "-jar", "calc.jar"]