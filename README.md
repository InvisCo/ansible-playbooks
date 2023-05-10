# Ansible Playbooks Collection

This is a collection of Ansible Playbooks I created to setup various systems and applications in my home-lab environment.

## Usage Instructions

Follow the [Ansible Getting Started Guide](https://docs.ansible.com/ansible/latest/getting_started/index.html) and set up your inventory file.

Run the playbook you want with: `ansible-playbook -i <path-to-inventory> <path-to-playbook>`

_**Disclaimer:** Please check and edit the playbooks before running to ensure that only the changes that you want are made to your system._

**Note:** These playbooks are all written to be run on Debian-based remote machines. You may need to make some modifications for other operating systems.

## Reusable Tasks

### Get latest release version from GitHub

This task retrieves the version tag of the latest release from a specific GitHub repository. 

| Variable | Description                                           |
| -------- | ----------------------------------------------------- |
| gh_user  | The user/organization the repository belongs to       |
| gh_repo  | The repository you want to get the latest release for |
| version  | (OUTPUT) The version tag of the latest release        |

### Download a release asset from GitHub

This task downloads an asset from a release of a repository to a specified location. 

| Variable | Description                                                   |
| -------- | ------------------------------------------------------------- |
| gh_user  | The user/organization the repository belongs to               |
| gh_repo  | The repository you want to download the release from          |
| version  | The version tag of the release you want to download           |
| filename | The filename of the asset you want to download                |
| wk_dir   | The location on the filesystem you want to download the asset |