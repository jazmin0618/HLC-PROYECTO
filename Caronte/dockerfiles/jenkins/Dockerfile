FROM jenkins/jenkins:lts

USER root

#instalar kubectl
RUN curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -L -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl" \
    && chmod +x ./kubectl \
    && mv ./kubectl /usr/local/bin/

#verificar la instalacion de kubectl
RUN kubectl version --client

USER jenkins

