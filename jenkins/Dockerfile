FROM jenkins/jenkins:latest
ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"
COPY security.groovy /usr/share/jenkins/ref/init.groovy.d/security.groovy
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
WORKDIR /jenkinswd
USER root
VOLUME ["/opt/automation/jenkins-master:/var/jenkins_home", "/var/run/docker.sock:/var/run/docker.sock"]
