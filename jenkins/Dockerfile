FROM jenkins/jenkins:latest
MAINTAINER Capital terefe<capital.terefe@gmail.com>
USER root
RUN apt-get update \
      && apt-get install -y sudo \
      && rm -rf /var/lib/apt/lists/*
RUN sudo echo "America/New_York" > /etc/timezone
USER jenkins 
#to allow serenity to capture screenshots whithout security issues
ENV JAVA_OPTS="-Djava.awt.headless=true -Dhudson.model.DirectoryBrowserSupport.CSP=\"sandbox allow-forms allow-scripts; default-src 'self'; script-src 'self' 'unsafe-inline'; style-src 'self' 'unsafe-inline';\""
# Install plugins
RUN /usr/local/bin/install-plugins.sh \
git \
matrix-auth \
workflow-aggregator \
docker-workflow \
blueocean \
credentials-binding \
junit:1.24 \
htmlpublisher:1.16 \
ssh-agent:1.15 \
perfpublisher:8.05

# Skip initial setup
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false

COPY executors.groovy /usr/share/jenkins/ref/init.groovy.d/
COPY default-user.groovy /usr/share/jenkins/ref/init.groovy.d/
VOLUME /var/jenkins_home

ENV JENKINS_USER admin
ENV JENKINS_PASS admin

