# 🛠️ Configuration Management Project for [roadmap.sh](https://roadmap.sh/)

This is my solution to the [Configuration Management project](https://roadmap.sh/projects/configuration-management) in the [DevOps roadmap](https://roadmap.sh/devops) from [roadmap.sh](https://roadmap.sh/)

**Table of Contents**
- [Project Requirements](#project-requirements)
- [Prerequisites](#prerequisites)
- [Configuration Management](#configuration-management)
- [Author](#author)

## Project Requirements

- [ ] Write Ansbile playbook `setup.yaml`. When you run the playbook, it should run the roles above in sequence.
- [x] Write Ansible Role `base` (basic server setup (installs utilities, updates the server, installs `fail2ban`, etc.))
- [ ] Write Ansible role `nginx` (installs and configures `nginx`)
- [ ] Write Ansible role `app` (uploads the given tarball of a static HTML website to the server and unzips it)
- [x] Write Ansible role `ssh` (adds the given public key to the server)
- [x] Setup the inventory.ini to include the server you are going to configure
- [ ] You should also assign proper tags to the roles so that you can run only specific roles
- [ ] **Advanced**. Modify the app role to pull the repository from GitHub and deploy it

## Prerequisites

- A remote server (Ubuntu Server 22.04) with configured SSH access

## Configuration Management

**- `ssh` role**
  Variables:
    - `ssh_user`: username to deploy ssh key
    - `ssh_pubkey_path` local ssh public key path
  Usage:
    Redefine variables and run playbook with tag
```bash
# --tags run only ssh role tasks
# --ask-become-pass sudo password, can be specified in ansible.cfg become_password=password
ansible-playbook setup.yaml --tags ssh --ask-become-pass
```
**- `base` role**
  Variables:
    - `apt_packages`: apt packages to install
  Usage:
    Run playbook with tag
```bash
# --tags run only base role tasks
# --ask-become-pass sudo password, can be specified in ansible.cfg become_password=password
ansible-playbook setup.yaml --tags base --ask-become-pass
```

## Author

Sergey Torshin [@torshin5ergey](https://github.com/torshin5ergey)
