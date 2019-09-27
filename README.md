# Docker-DevOps-Setup

# Start swarm
* docker swarm init
* may have to use --advertise-addr if multiple addresses

# Set username and password for jenkins
* `echo "admin" | docker secret create jenkins-user -`
* `echo "admin" | docker secret create jenkins-pass -`

# Start docker stack
`docker stack deploy -c docker-compose.yml foo`

# Changing jenkins and gitlab images
* Dockerfiles for jenkins and gitlab images are stored in the dockerfiles folder
* jenkins plugins list and groovy config are in the jenkinsconfig folder

# Sources
https://technologyconversations.com/2017/06/16/automating-jenkins-docker-setup/
