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

