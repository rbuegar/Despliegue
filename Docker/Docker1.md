# Comandos instalacion docker

- sudo apt update
- sudo apt upgrade -y
- sudo apt install apt-transport-https ca-certificates curl gnupg2 software-properties-common -y
- curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
- echo "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list
- sudo apt update
- sudo apt install docker-ce -y
- sudo systemctl start docker
- sudo systemctl enable docker
- sudo docker --version
- sudo usermod -aG docker $USER
- sudo docker run hello-world.

## Foto docker finalizado
![] (https://github.com/rbuegar/Despliegue/blob/master/Docker/docker.jpg)

