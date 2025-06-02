FROM jenkins/jenkins:lts

USER root

# Instalar Docker CLI
RUN apt-get update && \
    apt-get install -y docker.io
    
#instalar kubectl
RUN curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -L -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl" \
    && chmod +x ./kubectl \
    && mv ./kubectl /usr/local/bin/

#verificar la instalacion de kubectl
RUN kubectl version --client

USER jenkins

