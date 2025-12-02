# 🚀 CI/CD Pipeline with Automated Deployment

A production-ready CI/CD pipeline that automates **testing, building, monitoring, and deployment** of a Node.js application using **GitHub Actions, Docker, and Prometheus**.


![Prometheus Metrics](./screenshots/prometheus-metrics2.png)


## ⭐ Project Highlights

- ✅ Fully automated CI/CD pipeline with GitHub Actions
- ✅ Docker containerization with multi-stage builds
- ✅ Automated testing with Jest and Supertest
- ✅ Docker images automatically pushed to Docker Hub
- ✅ Prometheus monitoring integration
- ✅ Health check endpoints
- ✅ Production-ready architecture


## 🛠 Tech Stack

|Category      |Technology|
|--------------|----------------|
|**Runtime**|Node.js, Express.js|
|**CI/CD**|GitHub Actions|
|**Containerization**|Docker, Docker Hub|
|**Testing**|Jest, Supertest|
|**Monitoring**|Prometheus (prom-client)|

## 📦 Docker Image

**Docker Hub**: `poojadasdev/nodejs-app`

Pull the latest image:

```docker
docker pull poojadasdev/nodejs-app:latest

```

## 🏗 Architecture

```
Developer → GitHub → CI Pipeline → Tests → Docker Build → Docker Hub → Deployment

```

## 🔁 CI/CD Workflow

### 🧪 1. Test Stage

- Install dependencies
- Run automated tests (Jest/Supertest)
- Validate code quality

### 🏗 2. Build Stage

- Build optimized Docker image
- Tag with `latest` and commit SHA
- Login to Docker Hub
- Push image to registry

### 🚀 3. Deploy Stage

- Deployment notifications
- Ready for cloud deployment integration



## 🚦 Getting Started

### Prerequisites

- Node.js
- Docker
- GitHub account
- Docker Hub account

### 🚀 Local Setup

```bash
# Clone the repository
git clone https://github.com/ThePoojaDas/nodejs-cicd-pipeline
cd nodejs-cicd-pipeline

# Install dependencies
npm install

# Run tests
npm test

# Access the application at http://localhost:3000
```

### 🐳 Docker Setup
```bash
# Build Docker image
docker build -t nodejs-app:latest .

# Run container
docker run -p 3000:3000 nodejs-app:latest

# Run in detached mode
docker run -d -p 3000:3000 --name nodejs-app nodejs-app:latest

# View logs
docker logs nodejs-app
```

## 🔧 GitHub Secrets Configuration

To enable the CI/CD pipeline, configure these secrets in your GitHub repository:

**Path** (`Settings → Secrets and variables → Actions → New repository secret`):


| Secret Name | Description |
| --- | --- |
| `DOCKER_USERNAME` | Docker Hub username |
| `DOCKER_PASSWORD` | Docker Hub password/token |

## 📈 API Endpoints

| Endpoint | Description |
| --- | --- |
| `/` | Welcome message |
| `/health` | Health check |
| `/metrics` | Prometheus metrics |


## 📡 Monitoring & Metrics

Prometheus metrics available at: **`/metrics`**

**Tracks:**

- Total HTTP requests
- Request method, route, and status
- Application and Node.js runtime metrics


## ✨ Features

- **Automated Testing**: Every commit triggers test suite
- **Docker Optimization**: Multi-stage builds for smaller images
- **Version Tagging**: Automatic versioning with commit SHA
- **Continuous Integration**: Automated build and test pipeline
- **Container Registry**: Images stored in Docker Hub
- **Production Ready**: Health checks and monitoring included

## 📸 Screenshots

  ### GitHub Actions Workflow
    
   ![GitHub Actions](./screenshots/github-actions.png)
    
  ### Running Application
    
   ![Application Running](./screenshots/app-running.png)
    
 ### Prometheus Metrics Dashboard
    
  ![Prometheus Metrics](./screenshots/prometheus-metrics1.png)
  
  ![Prometheus Metrics](./screenshots/prometheus-metrics2.png)

  ![Prometheus Metrics](./screenshots/prometheus-metrics3.png)

  ![Prometheus Metrics](./screenshots/prometheus-metrics4.png)

  ![Prometheus Metrics](./screenshots/prometheus-metrics5.png)


  ### Docker Hub Repository
  
  ![Docker Hub](./screenshots/docker-hub.png)  


## 🔄 Pipeline Stages Overview

1. **Code Push** → Triggers GitHub Actions
2. **Test** → Runs all unit tests
3. **Build** → Creates Docker image
4. **Push** → Uploads to Docker Hub
5. **Deploy** → Ready for deployment

## 👩‍💻 Author

**Pooja Das**

DevOps Engineer | CI/CD | Docker | GitHub Actions | Monitoring

- **GitHub**: [ThePoojaDas](https://github.com/ThePoojaDas)
- **Docker Hub**: [poojadasdev](https://hub.docker.com/repositories/poojadasdev)

## 📝 License

This project is open source and available under the [MIT License](https://www.notion.so/LICENSE).
