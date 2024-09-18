This guide explains how to create an Amazon EKS (Elastic Kubernetes Service) cluster using Terraform. The setup includes creating a VPC, subnets, an EKS cluster, and worker nodes.

Prerequisites
Ensure you have the following installed:

Terraform CLI
AWS CLI
kubectl
Also, configure the AWS CLI with an IAM user or role that has permissions to create an EKS cluster.

Steps
1. Create a Directory
Create a new directory to store all your Terraform configuration files and navigate into it.

2. Define the AWS Provider
Create a Terraform configuration file to define the AWS provider and region for your infrastructure.

3. Set Input Variables
Define input variables to customize your EKS cluster configuration, such as cluster name, region, instance type, and node group settings.

4. Create a VPC
Configure a VPC with public and private subnets for the EKS cluster.

5. Define the EKS Cluster and Node Groups
Set up the EKS cluster and configure node groups with desired capacity, instance types, and other scaling options.

6. Output Cluster Details
Define outputs for important details like the cluster endpoint, security group IDs, and node group role ARNs.

7. Initialize and Apply Terraform
Initialize the Terraform working directory, plan the changes, and apply the configuration to deploy the EKS cluster and associated resources.

8. Configure kubectl
After the cluster is created, configure kubectl to interact with the EKS cluster using AWS CLI.

9. Verify the Cluster
Use kubectl to verify that the EKS cluster and its nodes are up and running.

Cleanup
To remove all resources, run the Terraform destroy command to delete the infrastructure.

Set Script Behavior:

set -e: Ensures the script exits immediately if any command fails.
exec >> /var/log/init-script.log 2>&1: Logs all output and errors to /var/log/init-script.log.
Update System:

sudo apt update -y: Updates package lists.
Install Docker:

sudo apt install docker.io -y: Installs Docker.
sudo usermod -aG docker ubuntu: Adds the ubuntu user to the Docker group.
sudo systemctl enable --now docker: Enables and starts Docker service.
Install AWS CLI:

Downloads and installs the AWS CLI.
Install Kubectl:

Downloads and installs Kubectl, the Kubernetes command-line tool.
Install eksctl:

Downloads and installs eksctl for managing EKS clusters.
Install Terraform:

Adds HashiCorp’s APT repository, then installs Terraform.
Install Trivy:

Installs Trivy, a vulnerability scanner for container images.
Install Argo CD:

Uses Kubectl to create a namespace and install Argo CD.
Install Helm:

Installs Helm, a package manager for Kubernetes.
Add Helm Repositories:

Adds repositories for Prometheus, Grafana, and ingress-nginx.
Install Prometheus, Grafana, and ingress-nginx:

Uses Helm to install Prometheus, Grafana, and ingress-nginx in Kubernetes.
This script sets up a comprehensive environment for Kubernetes and AWS, including monitoring and continuous deployment tools. Make sure you run this script with proper permissions and adjust it to fit your specific needs.



