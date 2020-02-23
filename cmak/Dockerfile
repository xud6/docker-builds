FROM wolfogre/kafka-manager:latest as builder
RUN mkdir /opt/out
RUN unzip /opt/*.zip -d /opt/out
RUN mv /opt/out/cmak* /opt/cmak
RUN ls -al /opt/cmak

FROM openjdk:11-jre-slim
RUN mkdir -p /app
RUN useradd appdeploy
RUN chown -R appdeploy:appdeploy /app
USER appdeploy
WORKDIR /app/
COPY --from=builder /opt/cmak ./
RUN ls -F
RUN which java

EXPOSE 9000

CMD bin/cmak