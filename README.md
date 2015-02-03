Ansible
=========
[![Build Status](https://travis-ci.org/docker/docker-registry.png)](https://git.tt-tech.de/iproject/iproject-dm/tree/develop)

If you don't install service mysql, please install it:
- Install mysql: `apt-get install mysql-server`

Here this is way to we deploy the project with Ansible Playbook

- Local (Beginer and Deploy as Server Test)
  - `cd ~/Ansible`
  - `ansible-playbook -i hosts site.yml`

- Server Test
  - `cd ~/Ansible`
  - `ansible-playbook -i hosts site_test.yml -u bachviet --ask-sudo-pass`
