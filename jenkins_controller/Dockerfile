FROM jenkins/jenkins:2.414.2-lts-jdk17

ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"

COPY plugins.txt /usr/share/jenkins/ref/

USER root

RUN apt-get update \
    && apt-get install -y python3 python3-pip \
    && jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt

USER jenkins

