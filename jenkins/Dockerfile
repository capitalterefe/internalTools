FROM jenkins/jenkins:2.128
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
RUN /usr/local/bin/RUN /usr/local/bin/install-plugins.sh \
pipeline-rest-api:2.10 \
script-security:1.44 \
command-launcher:1.2 \
handlebars:1.1.1 \
cloudbees-folder:6.4 \
jsch:0.1.54.2 \
bouncycastle-api:2.16.3 \
docker-commons:1.13 \
structs:1.14 \
workflow-step-api:2.15 \
docker-workflow:1.17 \
scm-api:2.2.7 \
workflow-api:2.27 \
junit:1.24 \
antisamy-markup-formatter:1.5 \
token-macro:2.5 \
git-client:2.7.2 \
build-timeout:1.19 \
credentials:2.1.16 \
ssh-credentials:1.13 \
git-server:1.7 \
plain-credentials:1.4 \
workflow-cps-global-lib:2.9 \
credentials-binding:1.16 \
timestamper:1.8.10 \
workflow-support:2.18 \
github-api:1.92 \
durable-task:1.22 \
pipeline-graph-analysis:1.6 \
workflow-durable-task-step:2.19 \
matrix-project:1.13 \
display-url-api:2.2.0 \
resource-disposer:0.8 \
ws-cleanup:0.34 \
ant:1.8 \
git:3.9.1 \
gradle:1.28 \
pipeline-milestone-step:1.3.1 \
jquery-detached:1.2.1 \
jackson2-api:2.8.11.3 \
github:1.29.1 \
ace-editor:1.1 \
mailer:1.21 \
workflow-scm-step:2.6 \
workflow-cps:2.53 \
pipeline-input-step:2.8 \
branch-api:2.0.20 \
pipeline-stage-step:2.3 \
workflow-job:2.21 \
momentjs:1.1.1 \
pipeline-stage-view:2.10 \
workflow-multibranch:2.19 \
pipeline-build-step:2.7 \
authentication-tokens:1.3 \
pipeline-model-api:1.2.9 \
mapdb-api:1.0.9.0 \
pipeline-model-extensions:1.2.9 \
apache-httpcomponents-client-4-api:4.5.5-2.1 \
workflow-basic-steps:2.7 \
pipeline-stage-tags-metadata:1.2.9 \
pipeline-model-declarative-agent:1.1.1 \
pipeline-model-definition:1.2.9 \
workflow-aggregator:2.5 \
github-branch-source:2.3.6 \
pipeline-github-lib:1.0 \
subversion:2.10.6 \
ssh-slaves:1.26 \
matrix-auth:2.2 \
pam-auth:1.3 \
ldap:1.20 \
email-ext:2.62 \
htmlpublisher:1.16 \
ssh-agent:1.15 \
performance:3.10 \
perfpublisher:8.05

