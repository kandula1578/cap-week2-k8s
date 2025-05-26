# AWS EKS Final Project — Events App (Node.js + MySQL)
This project is a simple RESTful backend API built using Node.js and Express, with MySQL as the data store. It serves event data and demonstrates deployment-ready microservice architecture for AWS EKS.

## Technology Stack
Node.js (Express.js)
MySQL
Docker
Kubernetes (kubectl)
eksctl
Terraform
Helm
Git

## Prerequisites
Make sure you're running Amazon Linux 3 or an equivalent Linux distribution.

Install All Dependencies
To install Docker, Kubernetes CLI (kubectl), eksctl, Git, Node.js, Terraform, and Helm use below commands

Installing Docker

<sub sudo yum install -y docker
     sudo systemctl enable docker
     sudo systemctl start docker  sub>

Installing git

sudo yum install -y git

Installing Node.js (LTS) using NVM...

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc
nvm install --lts

Installing kubectl

curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.31.2/2024-11-15/bin/linux/amd64/kubectl
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
kubectl version --client

Installing eksctl

ARCH=amd64
PLATFORM=$(uname -s)_$ARCH
curl -sLO "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_${PLATFORM}.tar.gz"
tar -xzf eksctl_${PLATFORM}.tar.gz -C /tmp
sudo mv /tmp/eksctl /usr/local/bin
rm eksctl_${PLATFORM}.tar.gz
eksctl version

Installing Terraform

sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/AmazonLinux/hashicorp.repo
sudo yum install -y terraform
terraform -version

Installing helm

curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
chmod 700 get_helm.sh
./get_helm.sh
