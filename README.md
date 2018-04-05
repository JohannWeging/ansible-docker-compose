# JohannWeging.docker-compose
Ansible role for deploying docker compose files.

## Usage
The role uses the template module to template compose files to the remove host.
This allows for ansible variables and jinja2 templating to be used in a docker compose file.

## Variables
```yaml
# set the project name to directory name of the ansible porject
docker_compose_project: "{{ playbook_dir | basename }}"
# set the compose file template path
docker_compose_file_path: "{{ playbook_dir }}/compose-files/docker-compose.yml"
# if docker compose should pull new images first
docker_compose_pull: true
```

# README Generation
To generate the readme use MarkdownPP
```
# pip install MarkdownPP
$ markdown-pp README.md.mdpp -o README.md
```
