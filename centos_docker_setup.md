# Uninstall old versions 
### Source - https://docs.docker.com/engine/install/centos/
```bash
sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine
```

# Docker Install 
```bash
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```
# Start Docker
```bash
sudo systemctl start docker
```
### Verify that the Docker Engine installation is successful by running the hello-world image.
```bash
sudo docker run hello-world
```
# Docker Composer install 
### Source - https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-centos-7
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
# Step - 2
```bash
sudo chmod +x /usr/local/bin/docker-compose
```
# docker-compose --version
```bash
docker-compose --version
```

### Port issue solve - https://stackoverflow.com/questions/50665028/docker-error-for-nginx-cannot-start-service-nginx-driver-failed-programming-ex
