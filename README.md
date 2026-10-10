# AWS EKS 2048 Game Deployment

Deploy the classic 2048 web game on Amazon EKS using AWS Fargate, Kubernetes, and the AWS Load Balancer Controller.

## Architecture

- **Amazon EKS** — managed Kubernetes control plane
- **AWS Fargate** — serverless compute for Kubernetes pods
- **Kubernetes Deployment** — runs five replicas of the 2048 application
- **Kubernetes Service** — exposes the application internally to the ingress
- **AWS Load Balancer Controller** — provisions and manages the Application Load Balancer
- **Application Load Balancer (ALB)** — provides public HTTP access to the game

### Request flow

Browser → Internet-facing ALB → Kubernetes Ingress → Kubernetes Service → 2048 Pods

## Project Structure

```text
aws-eks-game-deployment/
├── k8s/
│   └── 2048_full.yaml
├── screenshots/
├── .gitignore
└── README.md

