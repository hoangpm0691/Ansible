# Ansible
[![Build Status](https://travis-ci.org/docker/docker-registry.png)](https://git.tt-tech.de/iproject/iproject-dm/tree/develop)

If you don't install service mysql & apache, please install it:
- First update system: `sudo apt-get update`
- Install mysql & apache: `sudo apt-get install mysql-server apache2`

Here this is way to we deploy the project with Ansible Playbook

### Local 
1. Local for Beginner:

  - Copy database to `roles/local_beginner/templates/data/`
  - Rename file that you have just copied to `bachviet.sql`
  - Change value of the variable `tag_name` in file `group_vars/tags` to your name tag
  - `cd ~/Ansible`
  - `ansible-playbook -i hosts site_beginner.yml`
  
1. Local for Deploy Test:

  - Change value of the variable `tag_name` in file `group_vars/tags` to your name tag
  - `cd ~/Ansible`
  - `ansible-playbook -i hosts site_deploy.yml`

### Server Test:

  - Change value of the variable `tag_name` in file `group_vars/servertest` to your name tag
  - `cd ~/Ansible`
  - `ansible-playbook -i hosts site_test.yml -u bachviet --ask-sudo-pass`

### Server Live:

1. Beginer:

  - Change value of the variable `tag_name` in file `group_vars/staging_live` to your name tag
  - Add ansible_sudo_pass in file `hosts`
  - Edit config database in `config.yml` of role `live_begin`
  - `./deploy_on_serverlive_begin.sh`

1. Next deploy time:

  - Change value of the variable `tag_name` in file `group_vars/staging_live` to your name tag
  - Add ansible_sudo_pass in file `hosts`
  - Edit config database in `config.yml` of role `live_deploy`
  - `./deploy_on_serverlive.sh`
