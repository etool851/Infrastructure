FROM jenkins/ssh-agent:5.12.0-jdk17

ENV DEBIAN_FRONTEND=noninteractive

USER root 

RUN apt-get update && apt-get install -y curl python3 python3-pip unzip ansible git

RUN groupadd -g 997 docker && usermod -aG docker jenkins

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && unzip awscliv2.zip && ./aws/install

RUN curl -fsSL https://get.docker.com -o get-docker.sh && sh ./get-docker.sh

RUN curl -SL https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64 -o /usr/local/bin/docker-compose && chmod +x /usr/local/bin/docker-compose


