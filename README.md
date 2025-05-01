# 🛠️ Configuration Management Project for [roadmap.sh](https://roadmap.sh/)

This is my solution to the [Configuration Management project](https://roadmap.sh/projects/configuration-management) in the [DevOps roadmap](https://roadmap.sh/devops) from [roadmap.sh](https://roadmap.sh/)

**Table of Contents**
- [Project Requirements](#project-requirements)
- [Prerequisites](#prerequisites)
- [Configuration Management](#configuration-management)
- [Author](#author)

## Project Requirements

- [ ] Write Ansbile playbook `setup.yaml`. When you run the playbook, it should run the roles above in sequence.
- [ ] Write Ansible Role `base` (basic server setup (installs utilities, updates the server, installs `fail2ban`, etc.))
- [ ] Write Ansible role `nginx` (installs and configures `nginx`)
- [ ] Write Ansible role `app` (uploads the given tarball of a static HTML website to the server and unzips it)
- [ ] Write Ansible role `ssh` (adds the given public key to the server)
- [ ] Setup the inventory.ini to include the server you are going to configure
- [ ] You should also assign proper tags to the roles so that you can run only specific roles
- [ ] **Advanced**. Modify the app role to pull the repository from GitHub and deploy it

## Prerequisites

- A remote server (Ubuntu Server 22.04) with configured SSH access

## Configuration Management

## Author

Sergey Torshin [@torshin5ergey](https://github.com/torshin5ergey)
