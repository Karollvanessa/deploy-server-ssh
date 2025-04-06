# deploy-server-ssh
Exercise on how to implement the Backend on a Remote Server via SSH.

# Remote Backend Deployment using SSH and GitHub Actions

## Overview

This repository demonstrates how to deploy a backend (API or web application) to a remote server using SSH access secured by public/private key authentication, and GitHub Actions for automation.

## Prerequisites

- A remote server with SSH access
- GitHub repository with deployment scripts
- SSH key pair (private key added to GitHub Secrets)
- Public key added to the server's `~/.ssh/authorized_keys`

## Steps

### 1. Repository Setup

First, the repository was created in **GitHub**. Then, we navigated to the **Actions** tab to configure GitHub Actions for deployment automation.

### 2. GitHub Secrets Configuration

In **Repository Settings > Secrets and variables > Actions**, we added the following secrets:

- `SSH_PRIVATE_KEY`: The private key generated on local machine
- `SSH_HOST`: The IP address or hostname of the remote server (e.g., `191.89.129.146`)
- `USER_NAME`: The username for SSH (e.g., `ndgServer`)
- `PROJECT_PATH`: The path on the remote server where the project should be deployed (e.g., `/home/ndgServer/project`)
- `GIT_REPO`: URL of this GitHub repository

### 3. Connecting to Remote Server

From terminal, we used the following command to connect:

```bash
ssh -i pemSMacServerEstudiantes ndgServer@201.190.115.29