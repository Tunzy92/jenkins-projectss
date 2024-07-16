Jenkins setup on AWS Autoscaling group, Load Balancer and EFS using Terraform, Packer and Ansible

![Readme](https://github.com/user-attachments/assets/f30b219a-261d-4e88-a8e2-5695af7f9ff9)

In this project, you will learn how to deploy Jenkins on an AWS Autoscaling group with an Application Load Balancer and EFS filesystem for Jenkins’ data directory.

We aim to implement the following concepts in the project.

Immutable Infrastructure
Infrastructure as Code (Provisioning & Configuration Management)
External Config/Secret management

                                        TOOLS & SERVICES USED
For this Jenkins project, I have used the following DevOps Tools

GitHub: Repository to store IaC
Packer: To build Jenkins Controller and agent AMIs
Ansible: To configure Jenkins controller and agent during the AMI building process
Terraform: To provision AWS resources
Python Boto3: To retrieve SSH public key from AWS parameter store.
Following are the AWS services used.

IAM: To create IAM Role/Instance Profile for Jenkins Controller and Agent Nodes.
EFS: To store Jenkins data
AWS Parameter Store: To store SSH private and public keys as secrets to configure agents.
Autoscaling Group: To deploy the Jenkins controller
Application Load Balancer: To have a static DNS endpoint for the Jenkins controller instance running in the autoscaling group.
We will be using the default VPC in the us-west-2 (Oregon) region. There will be four default subnets. We will be using three subnets from the following three availability zones:

us-east-1a
us-east-1b
us-east-1c
Ensure you have an existing key pair in your AWS account for the N-virginia region. We will use it with instances to enable SSH access.

Detailed walkthrough here https://medium.com/@onabanjo.temitayo3/jenkins-setup-project-on-aws-using-autoscaling-group-terraform-packer-and-ansible-b0ed8c5abbf5
