# Ansible
[![Build Status](https://travis-ci.org/docker/docker-registry.png)](https://git.tt-tech.de/iproject/iproject-dm/tree/develop)

If you don't install service mysql & apache, please install it:
- First update system: `sudo apt-get update`
- Install mysql & apache: `sudo apt-get install mysql-server apache2`

Here this is way to we deploy the project with Ansible Playbook

- Local for Beginner:
  - Change value of the variable `tag_name` in file `group_vars/tags` to your name tag
  - `cd ~/Ansible`
  - `ansible-playbook -i hosts site_beginner.yml`
  
- Local for Deploy Test:
  - Change value of the variable `tag_name` in file `group_vars/tags` to your name tag
  - `cd ~/Ansible`
  - `ansible-playbook -i hosts site_deploy.yml`

- Server Test
  - Change value of the variable `tag_name` in file `group_vars/servertest` to your name tag
  - `cd ~/Ansible`
  - `ansible-playbook -i hosts site_test.yml -u bachviet --ask-sudo-pass`
