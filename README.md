# Docker-DevOps-Setup
* Still in progress. Working on Mimicing DinD without actually spawning child containers. Instead I am trying to spawn sibling containers
* https://itnext.io/docker-in-docker-521958d34efd
# Start swarm
* docker swarm init
* may have to use `docker swarm init --advertise-addr XXXXXXXX` if multiple addresses

# Set username and password for jenkins
* `echo "admin" | docker secret create jenkins-user -`
* `echo "admin" | docker secret create jenkins-pass -`

# Start docker stack
`docker stack deploy -c docker-compose.yml foo`

# Changing jenkins and gitlab images
* Dockerfiles for jenkins and gitlab images are stored in the dockerfiles folder
* jenkins plugins list and groovy config are in the jenkinsconfig folder
# Issues
* Gitlab keeps reporting an unhealthy state and swarm reboots it each time. Need to fix

# Sources
https://technologyconversations.com/2017/06/16/automating-jenkins-docker-setup/
