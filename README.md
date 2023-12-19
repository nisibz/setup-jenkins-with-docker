# Jenkins with Docker Setup

This repository provides an example setup for running Jenkins with Docker using Docker Compose.

## Prerequisites

- Docker
- Docker Compose

## Usage

1. Clone this repository:

   ```bash
   git clone https://github.com/nisibz/setup-jenkins-with-docker.git
   cd setup-jenkins-with-docker
   ```

2. Create a Docker network for Jenkins:

   ```bash
   docker network create jenkins
   ```

3. Start the Jenkins and Docker containers:

   ```bash
   docker compose up -d
   ```

4. Access Jenkins:

   Open your web browser and go to http://localhost:8080

5. Get automatically-generated alphanumeric password.

   ```bash
   sudo docker exec jenkins-blueocean cat /var/jenkins_home/secrets/initialAdminPassword
   ```

## Clean up

To stop and remove the containers and volumes created by Docker Compose, run:

```bash
docker compose down -v
```
