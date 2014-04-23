# Ansible Docker module presentation

This repository contains samples of how one would utilize the docker and docker_images Ansible modules to build images and launch them

## Requirements

* Set up python virtualenv
* Clone the ansible source repository (https://github.com/ansible/ansible.git)
* Set up your paths to run ansible from the source directory you checked out 
    ../ansible/hacking/env-setup.sh
* Obtain the docker image building repository

## Setup

* Set up your vars files for whatever values you require
  * number of containers per type
  * name of your Docker repository

## Usage

* Build your images
    ansible-playbook -i hosts -vvvv images.yml
* Launch your images
    anbible-playbook -i hosts -vvvv site.yml
* Destory your images
    anbible-playbook -i hosts -e "ansible_state=absent" -vvvv site.yml
