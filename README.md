# Docker Compose 

A multi-service Docker application demonstrating Docker Compose .

## Services
- Movies (Port 91)
- Documentaries (Port 92)
- Animations (Port 93)
- Webseries (Port 94)

## Prerequisites
- Docker
- Docker Compose

## Installation

### Install Docker
```bash
sudo yum install docker -y
sudo systemctl start docker
sudo systemctl enable docker
```

### Install Docker Compose
```bash
sudo curl -L "https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
docker-compose --version
```

## Building Images

Build individual images for each service:
```bash
# Movies
docker build -t movies:v1 .

# Documentaries (modify index.html heading first)
docker build -t documentaries:v1 .

# Animations (modify index.html heading first)
docker build -t animations:v1 .

# Webseries (modify index.html heading first)
docker build -t webseries:v1 .
```

## Usage

### Start all services
```bash
docker-compose up -d
```

### Access services
- Movies: http://YOUR_IP:91
- Documentaries: http://YOUR_IP:92
- Animations: http://YOUR_IP:93
- Webseries: http://YOUR_IP:94

### Stop all services
```bash
docker-compose down
```

## Docker Compose Commands
```bash
docker-compose up -d        # Start services in detached mode
docker-compose down         # Stop and remove containers
docker-compose stop         # Stop containers
docker-compose start        # Start stopped containers
docker-compose restart      # Restart services
docker-compose ps           # List running services
docker-compose logs         # View logs
docker-compose pause        # Pause services
docker-compose unpause      # Resume services
```

