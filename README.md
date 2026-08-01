<p align="center">
  <a href="./wordpress-userdata/">
    <img src="https://github.com/user-attachments/assets/b89f7e56-58fe-4f56-ad8d-eba434331ed6"
         width="465"
         alt="WordPress Userdata Deployment">
  </a>

  <a href="./nginx-cloud-init/">
    <img src="https://github.com/user-attachments/assets/330646f2-97f3-4c9f-b62d-157d81a15151"
         width="489"
         alt="NGINX Cloud-Init Deployment">
  </a>
</p>

<p align="center">
  <a href="./wordpress-userdata/"><strong>WordPress Userdata Deployment</strong></a>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <a href="./nginx-cloud-init/"><strong>NGINX Cloud-Init Deployment</strong></a>
</p>

<h1 align="center">Terraform EC2 Provisioning Setups</h1>

<p align="center"><strong>The free, open-source Azure emulator. Develop and test your Azure apps locally.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/Terraform-5C4EE5?logo=terraform&logoColor=white" alt="Terraform">
  <img src="https://img.shields.io/badge/Bash-4EAA25?logo=gnu-bash&logoColor=white" alt="Bash">
  <img src="https://img.shields.io/badge/Cloud--Init-6DB33F?logo=cloud-init&logoColor=white" alt="Cloud-Init">
  <img src="https://img.shields.io/badge/AWS-FF9900?logo=amazon-aws&logoColor=white" alt="AWS">
  <img src="https://img.shields.io/badge/EC2-FF9900?logo=amazon-aws&logoColor=white" alt="EC2">
  <img src="https://img.shields.io/badge/NGINX-009639?logo=nginx&logoColor=white" alt="NGINX">
  <img src="https://img.shields.io/badge/Apache-CA1F00?logo=apache&logoColor=white" alt="Apache">
  <img src="https://img.shields.io/badge/PHP-777BB4?logo=php&logoColor=white" alt="PHP">
  <img src="https://img.shields.io/badge/WordPress-21759B?logo=wordpress&logoColor=white" alt="WordPress">
</p>

<p align="center">Local Azure development. One binary. No account needed.</p>

> **Disclaimer:** miniblue is an independent open-source project. It is not affiliated with, endorsed by, or associated with Microsoft or Azure.

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
  <img src="https://github.com/user-attachments/assets/b89f7e56-58fe-4f56-ad8d-eba434331ed6" width="500" alt="AWS/Terraform Architecture Diagram"> 
</p>

### 2. NGINX Cloud-Init Deployment  
A lightweight EC2 deployment that uses cloud-init to install and configure NGINX during instance boot.  
Shows how to use declarative YAML for cleaner provisioning and easier maintenance.

<p align="center">
  <img src="https://github.com/user-attachments/assets/330646f2-97f3-4c9f-b62d-157d81a15151" width="500" alt="AWS/Terraform Architecture Diagram">
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
