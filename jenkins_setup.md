# Setting Up Jenkins in Docker

## Overview
In this step, we set up Jenkins in a Docker container, providing a platform to automate our CI/CD pipeline.

## Steps

### 1. Pull the Jenkins Docker Image
We pulled the official Jenkins image to ensure we had the latest Long-Term Support (LTS) version:
```bash
docker pull jenkins/jenkins:lts
```

### 2. Run the Jenkins Container
To run Jenkins, we used the following command, mapping the necessary ports and setting up a volume for persistent data:
```bash
docker run -d -p 8080:8080 -p 50000:50000 \
    --name jenkins \
    -v jenkins_home:/var/jenkins_home \
    jenkins/jenkins:lts
```

### 3. Check the Jenkins Container
We confirmed Jenkins was running using:
```bash
docker ps
```

### 4. Access Jenkins
- Opened a browser and navigated to `http://<your-server-ip>:8080`.

### 5. Retrieve Admin Password
We obtained the initial admin password to log in:
```bash
docker exec -it jenkins cat /var/jenkins_home/secrets/initialAdminPassword
```

### 6. Complete Setup
- Installed suggested plugins.
- Created an admin user.
- Configured the instance URL.

---

## Why These Steps?
1. **Dockerized Jenkins**: Simplifies setup and ensures portability.
2. **Persistent Volume**: Ensures Jenkins data is retained between container restarts.
3. **Port Mapping**: Provides access to the Jenkins UI and agent communication.
4. **Admin Password**: Required for secure access to Jenkins.

---
