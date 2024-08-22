# Before run
Don't forget to change `GF_SECURITY_ADMIN_PASSWORD` in `docker-compose.yml` file

## Requirements
- Docker
- docker-compose

# Run prometheus/grafana server
```shell
docker-compose up --build -d
```
Than open `http://localhost:3000` in web browser and login

# How to set up node-exporter
```shell
sudo docker pull prom/node-exporter

sudo docker run -d \
    -p 9100:9100 \
    prom/node-exporter
```
or install with out Docker
```shell
# x64
sudo wget https://github.com/prometheus/node_exporter/releases/download/v1.4.0/node_exporter-1.4.0.linux-amd64.tar.gz
sudo tar xvfz node_exporter-1.4.0.linux-amd64.tar.gz
cd node_exporter-1.4.0.linux-amd64
./node_exporter &

# ARM
wget https://github.com/prometheus/node_exporter/releases/download/v1.4.0/node_exporter-1.4.0.linux-arm64.tar.gz
tar xvfz node_exporter-1.4.0.linux-arm64.tar.gz
cd node_exporter-1.4.0.linux-arm64
./node_exporter &
```
