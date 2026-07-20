# Docker Deployment Guide

## Local Setup
```bash
docker build -t portfolio-website .
docker run -d -p 8080:80 portfolio-website
```

## EC2 Deployment
```bash
ssh -i portfolio-key.pem ubuntu@54.123.45.67
git clone https://github.com/username/portfolio.git
cd portfolio
docker build -t portfolio-website .
docker run -d -p 80:80 portfolio-website
```

## Useful Commands
```bash
docker images          # List images
docker ps             # Running containers
docker stop CONTAINER_ID
docker logs CONTAINER_ID
```