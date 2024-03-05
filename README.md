# Deep learning project with deployments in azure and aws

## workflows

- Update config.yaml
- Update params.yaml
- Update the entity
- Update the configuration manager in src config
- Update the components
- Update the pipeline
- Update the main.py
- Update the dvc.yaml

# AWS-CICD-Deployment-with-Github-Actions

#with specific access

- EC2 access : It is virtual machine
- ECR: Elastic Container registry to save your docker image in aws

#Description: About the deployment

1. Build docker image of the source code
2. Push your docker image to ECR
3. Launch Your EC2 
4. Pull Your image from ECR in EC2
5. Lauch your docker image in EC2

#Policy:

1. AmazonEC2ContainerRegistryFullAccess
2. AmazonEC2FullAccess

# Create ECR repo to store/save docker image
- Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/<project_name>
# Create EC2 machine (Ubuntu)

# Open EC2 and Install docker in EC2 Machine:
#optinal
sudo apt-get update -y
sudo apt-get upgrade

#required
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker

#Configure EC2 as self-hosted runner:
setting>actions>runner>new self hosted runner> choose os> then run command one by one

# Setup github secrets:
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_REGION = us-east-1
AWS_ECR_LOGIN_URI = 
ECR_REPOSITORY_NAME = simple-app

## AZURE-CICD-Deployment-with-Github-Actions
Save pass:
# Run from terminal:
docker build -t <app_name>.azurecr.io/<app_name>:latest .
docker login <app_name>.azurecr.io
docker push <app_name>.azurecr.io/<app-name>:latest

# Deployment Steps:
Build the Docker image of the Source Code
Push the Docker image to Container Registry
Launch the Web App Server in Azure
Pull the Docker image from the container registry to Web App server and run





