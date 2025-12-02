# 🚀 CI/CD Pipeline with Automated Deployment

A production-ready CI/CD pipeline that automates **testing, building, monitoring, and deployment** of a Node.js application using **GitHub Actions, Docker, and Prometheus**.

## ⭐ Project Highlights

- ✅ Fully automated CI/CD pipeline with GitHub Actions
- ✅ Docker containerization with multi-stage builds
- ✅ Automated testing with Jest and Supertest
- ✅ Docker images automatically pushed to Docker Hub
- ✅ Prometheus monitoring integration
- ✅ Health check endpoints
- ✅ Production-ready architecture

## 📦 Docker Image

**Docker Hub**: `poojadasdev/nodejs-app`

Pull the latest image:

```docker
docker pull poojadasdev/nodejs-app:latest

```

## 🛠 Tech Stack

- **Application**: **Node.js, Express.js**
- **CI/CD:** **GitHub Actions**
- **Containerization: Docker & Docker Hub**
- **Testing:** **Jest + Supertest**
- **Monitoring:** **Prometheus (prom-client)**

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

## 📡 Monitoring & Metrics

Prometheus metrics available at: **`/metrics`**

**Tracks:**

- Total HTTP requests
- Request method, route, and status
- Application and Node.js runtime metrics

## 🚦 Getting Started

### Prerequisites

- Node.js
- Docker
- GitHub account
- Docker Hub account

### 🚀 Local Setup

```bash
*# Clone the repository*
git clone https://github.com/ThePoojaDas/nodejs-cicd-pipeline
cd nodejs-cicd-pipeline

*# Install dependencies*
npm install

*# Run tests*
npm test

*# Build Docker image*
docker build -t nodejs-app:latest .

*# Run container*
docker run -p 3000:3000 nodejs-app:latest
```

## 🔧 GitHub Secrets Configuration

Set these secrets in your GitHub repository (`Settings → Secrets and variables → Actions`):

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

## ✨ Features

- **Automated Testing**: Every commit triggers test suite
- **Docker Optimization**: Multi-stage builds for smaller images
- **Version Tagging**: Automatic versioning with commit SHA
- **Continuous Integration**: Automated build and test pipeline
- **Container Registry**: Images stored in Docker Hub
- **Production Ready**: Health checks and monitoring included

## 📸 Screenshots

- GitHub Actions workflow
    
    ![image.png](attachment:0068e8b3-1cc5-4bbf-a5c9-de5c65b5820f:image.png)
    
- Running application
    
    ![image.png](attachment:267747f1-e728-4d60-a480-784c5ac16017:image.png)
    
    - Prometheus metrics dashboard
    
    ![image.png](attachment:68ccffb4-0927-41b6-91e2-a6c615a8f76a:image.png)
    
    ![image.png](attachment:47b12b82-1081-4470-8e95-190133c65a1f:image.png)
    
    ![image.png](attachment:92506dc7-9801-4137-b6bd-5b3578a04640:image.png)
    
    ![Screenshot 2025-12-02 at 5.51.24 PM.png](attachment:4ddbdb4d-cb48-4905-ba3f-7ba08c98c3b4:Screenshot_2025-12-02_at_5.51.24_PM.png)
    
    ![image.png](attachment:82178cfe-0de3-4387-8896-cb585fe9afdc:image.png)
    

- Docker Hub repository
    
    ![Screenshot 2025-12-02 at 5.54.51 PM.png](attachment:93f39c0d-28f4-4f4f-821f-68dd8fa8932f:Screenshot_2025-12-02_at_5.54.51_PM.png)
    

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