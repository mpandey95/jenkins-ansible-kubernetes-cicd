# Jenkins Ansible Kubernetes CI/CD

![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white) ![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white) ![Maven](https://img.shields.io/badge/apache_maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white) ![Ansible](https://img.shields.io/badge/ansible-%231A1918.svg?style=for-the-badge&logo=ansible&logoColor=white) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)

---

**A comprehensive collection of Implementation documents** to build, configure, and automate a full-fledged robust DevOps CI/CD Pipeline from scratch.

This repository is designed to provide step-by-step guidance, configurations, and deployment strategies utilizing industry-standard tools including **Git, Jenkins, Maven, Ansible, Docker, and Kubernetes**.

## Use Case
This repository acts as a centralized knowledge base and implementation guide for setting up end-to-end continuous integration and continuous deployment (CI/CD) pipelines. It is ideal for teams or individuals looking to configure automation servers (Jenkins), integrate build tools (Maven), manage configuration (Ansible), and deploy applications seamlessly to containerized environments (Docker) and container orchestration platforms (Kubernetes).

## Architecture

```mermaid
flowchart LR
    Dev([Developer]) -->|Push Code| Git[Git Repository]
    Git -->|Webhook/Poll| Jenkins[Jenkins CI Server]
    
    subgraph Build Phase
        Jenkins -->|Compile & Package| Maven[Maven Build]
    end
    
    subgraph Deploy Phase
        Maven -->|Artifact| Ansible[Ansible Configuration]
    end
    
    subgraph Target Environments
        Ansible -.->|Deploy App| Tomcat[Tomcat Server]
        Ansible -.->|Build & Run| Docker[Docker Host]
        Ansible -.->|Deploy YAMLs| K8s[Kubernetes Cluster]
    end
```

## Tech Stack
- **Version Control:** Git
- **Continuous Integration:** Jenkins
- **Build Tool:** Apache Maven
- **Configuration Management:** Ansible
- **Containerization:** Docker
- **Orchestration:** Kubernetes
- **Web Server / App Server:** Apache Tomcat

## Project Structure
```text
.
├── Ansible/            # Ansible installation and setup notes
├── Docker/             # Docker installation, commands, and Dockerfiles
├── Jenkins/            # Jenkins installation, Git, and Maven integrations
├── Jenkins_Jobs/       # CI/CD Jenkins job templates and deployment guides
├── Kubernetes/         # K8s setup, deployment YAMLs, and Ansible/Jenkins integration
├── Tomcat/             # Apache Tomcat server installation steps
└── README.md           # Project documentation
```

## Key Workflows & Features
- **Jenkins CI Automation:** From fundamental Jenkins installations to plugin integrations (Git, Maven) and running automated maven builds.
- **Ansible Configuration Management:** Setting up Ansible on RHEL and integrating it with Jenkins for streamlined, agentless deployment tasks.
- **Containerization with Docker:** Dockerfile creation for custom images (Apache, Application specific), managing containers, and interacting with DockerHub.
- **Kubernetes Orchestration:** Step-by-step Kubernetes cluster setup, composing deployment and service YAML files (`valaxy-deploy.yml`, `valaxy-service.yml`), and orchestrating Jenkins-Ansible-K8s workflows.
- **Automated Deployments:** Ready-to-use playbooks and documentation for deploying applications directly to Tomcat servers or as containers in Docker/Kubernetes.

## Getting Started

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/mpandey95/jenkins-ansible-kubernetes-cicd.git
   cd jenkins-ansible-kubernetes-cicd
   ```

2. **Explore the Modules:**
   Navigate through specific module folders based on your requirement:
   - For Jenkins CI setup, view the `Jenkins/` directory.
   - For writing automation playbooks, refer to the `Jenkins_Jobs/` and `Ansible/` guides.
   - For containerizing workloads, refer to the `Docker/` directory and progress to the `Kubernetes/` directory for orchestration.

3. **Follow Implementation Sub-Guides:**
   Inside each module, refer to the provided `.MD` files and templates in sequential order.

---

**Manish Pandey** — Senior DevOps/Platform Engineer

### 🛠️ Technology Stack
#### ☁️ Cloud & Platforms
![GCP](https://img.shields.io/badge/GCP-Expert-blue?style=flat-square&logo=google-cloud)
![AWS](https://img.shields.io/badge/AWS-Expert-FF9900?style=flat-square&logo=amazon-aws)

#### ⚙️ Platform & DevOps
![Kubernetes](https://img.shields.io/badge/Kubernetes-Expert-blue?style=flat-square&logo=kubernetes)
![Docker](https://img.shields.io/badge/Docker-Expert-2496ED?style=flat-square&logo=docker)
![Terraform](https://img.shields.io/badge/Terraform-Advanced-7B42BC?style=flat-square&logo=terraform)
![Helm](https://img.shields.io/badge/Helm-Advanced-0F1689?style=flat-square&logo=helm)
![Ansible](https://img.shields.io/badge/Ansible-Expert-EE0000?style=flat-square&logo=ansible)
![CI/CD](https://img.shields.io/badge/CI%2FCD-Expert-green?style=flat-square&logo=github-actions)

#### 🔐 Security & Ops
![IAM](https://img.shields.io/badge/IAM-Expert-red?style=flat-square)
![Networking](https://img.shields.io/badge/Networking-Advanced-blue?style=flat-square)
![Monitoring](https://img.shields.io/badge/Monitoring%20%26%20Logging-Expert-green?style=flat-square&logo=grafana)
![Secrets Management](https://img.shields.io/badge/Secrets%20Mgmt-Advanced-yellow?style=flat-square&logo=vault)

#### 🧑‍💻 Programming
![Python](https://img.shields.io/badge/Python-Advanced-3776AB?style=flat-square&logo=python)
![Bash](https://img.shields.io/badge/Bash-Advanced-4EAA25?style=flat-square&logo=gnu-bash)
![YAML](https://img.shields.io/badge/YAML-Advanced-CB171E?style=flat-square)

#### 💾 Database
![SQL](https://img.shields.io/badge/SQL-Advanced-CC2927?style=flat-square&logo=mysql)
![MongoDB](https://img.shields.io/badge/MongoDB-Advanced-13AA52?style=flat-square&logo=mongodb)

### Connect With Me
- **GitHub:** [@mpandey95](https://github.com/mpandey95)
- **LinkedIn:** [manish-pandey95](https://linkedin.com/in/manish-pandey95)
- **Email:** <mnshkmrpnd@gmail.com>

### License
See **LICENSE** | Support: [GitHub](https://github.com/mpandey95) • [LinkedIn](https://linkedin.com/in/manish-pandey95)
