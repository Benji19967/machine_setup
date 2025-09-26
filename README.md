# Machine Setup

The goal is to set up a new machine (e.g. laptop) with as minimal manual work as possible.

## 1.) SSH and GitHub

- Create an ssh key and add it to GitHub (see in notes repo: ssh.md)
- set git name and e-mail

## 2.) Clone this repo

Clone this repo in a dedicated coding workspace

## 3.) Ansible

## Install

`./ansible-install`

## Best practices

https://docs.ansible.com/ansible/2.8/user_guide/playbooks_best_practices.html

## Running a playbook

```bash
HOMEBREW_NO_AUTO_UPDATE=1 ansible-playbook -i local site.yml -c local
```

`-c local` tells Ansible not to try to connect through ssh but rather run the playbook 
(site.yml) locally.
