# graylog configure using docker composer on ubuntu
install docker
apt install docker.io
sudo systemctl start docker
sudo systemctl enable docker
install docker composer
sudo curl -L "https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version
#create docker composer file
sudo nano docker-compose.yml
echo -n yourpassword | sha256sum
sudo docker-compose up -d
