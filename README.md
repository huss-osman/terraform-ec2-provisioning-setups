# Terraform EC2 Provisioning Setups
<!-- Tooling -->
![Terraform](https://img.shields.io/badge/Terraform-5C4EE5?logo=terraform&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?logo=gnu-bash&logoColor=white)
![Cloud-Init](https://img.shields.io/badge/Cloud--Init-6DB33F?logo=cloud-init&logoColor=white)

<!-- AWS -->
![AWS](https://img.shields.io/badge/AWS-FF9900?logo=amazon-aws&logoColor=white)
![EC2](https://img.shields.io/badge/EC2-FF9900?logo=amazon-aws&logoColor=white)

<!-- Stack Technologies -->
![NGINX](https://img.shields.io/badge/NGINX-009639?logo=nginx&logoColor=white)
![Apache](https://img.shields.io/badge/Apache-CA1F00?logo=apache&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?logo=php&logoColor=white)
![WordPress](https://img.shields.io/badge/WordPress-21759B?logo=wordpress&logoColor=white)

## Overview

This repository contains two AWS Terraform deployments that showcase different ways to automate EC2 instance provisioning. 

Each setup focuses on a clean, reproducible workflow that demonstrates how Terraform, userdata and cloud-init can be used to configure instances on boot.

- The `wordpress-userdata` setup provisions an EC2 instance with Apache, PHP and WordPress installed through a userdata script.
- The `nginx-cloud-init` setup uses cloud-init to automate NGINX provisioning at boot in a clean and maintainable way.
  
These examples make it easy to compare approaches, understand the strengths of each and build more consistent infrastructure provisioning pipelines.

## Projects

### 1. WordPress Userdata Deployment  
A traditional userdata-driven EC2 configuration that installs Apache, PHP and WordPress automatically.  
Illustrates a script-based provisioning workflow that handles full server bootstrap via Bash.

<p align="center">
  <img src="https://github.com/user-attachments/assets/cfc609f5-fe98-40d0-8078-6a6640d11450" width="500" alt="AWS/Terraform Architecture Diagram"> 
</p>

### 2. NGINX Cloud-Init Deployment  
A lightweight EC2 deployment that uses cloud-init to install and configure NGINX during instance boot.  
Shows how to use declarative YAML for cleaner provisioning and easier maintenance.

<p align="center">
  <img src="https://github.com/user-attachments/assets/f8ef9ec6-3cca-4add-ace0-54939e9ae771" width="500" alt="AWS/Terraform Architecture Diagram">
</p>

## Repository Structure
```
Terraform-EC2-Provisioning-Setups
|
├── assets
│   ├── nginx-screenshot.png
│   ├── terminal-output.png
│   ├── tf-init.png                   # Architecture diagram for nginx-cloud-init
│   ├── tf-wordpress.png              # Architecture diagram for wordpress-userdata
│   └── wordpress-screenshot.png
|
├── nginx-cloud-init
│   ├── README.md
│   ├── cloud-init.yaml
│   ├── main.tf
│   ├── outputs.tf
│   ├── provider.tf
│   └── variables.tf
|
├── wordpress-userdata
│   ├── README.md
│   ├── main.tf
│   ├── outputs.tf
│   ├── provider.tf
│   ├── userdata.sh
│   └── variables.tf
|
└── .gitignore
```
