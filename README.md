# Machine Setup

The goal is to set up a new machine (e.g. laptop) with as minimal manual work as possible.

## 1.) SSH and GitHub

- Create an ssh key and add it to GitHub (see in notes repo: ssh.md)
- set git name and e-mail

## 2.) Clone this repo

Clone this repo in a dedicated coding workspace

## 3.) Ansible

Define a workspace:

```bash
export WORKSPACE=${HOME}/apps/home/labrecqb
```

Define an install dir (where binaries are installed and run from):

```bash
export INSTALL_DIR=...
```

Define config dir:

```bash
# static configs (e.g. nvim/init.lua)
export XDG_CONFIG_HOME=<labrecqb>/.config
# persisten data files (e.g. mason lsps)
export XDG_DATA_HOME=<labrecqb>/.local/share
# persistent state data (e.g. terminal history)
export XDG_STATE_HOME=<labrecqb>/.local/state
# non-essential cached data (e.g. compiler caches)
export XDG_CACHE_HOME=<labrecqb>/.cache
```

### 3.1) Installing

`./ansible-install-<os>`

### 3.2) Sudo without PW

This will forgo asking for a PW for the tasks that run as sudo (`become: true`).

```
sudo visudo
```

add 

```
<username> ALL=(ALL) NOPASSWD:ALL
```

to bottom of file (<username> is output of `whoami`)

### 3.3) Running the playbook

ubuntu:

`ansible-playbook ubuntu.yml`

macos:

`HOMEBREW_NO_AUTO_UPDATE=1 ansible-playbook macos.yml`

with a tag:

`ansible-playbook ubuntu.yml --tags "<tag_name>"`

## 4.) Neovim

Fix null-ls: https://github.com/Benji19967/notes/blob/master/vim.md#null-ls

### 4.1) Mason

Install Mason lsp tools (ruff, pyright, clangd)

## 5.) Python

see PYTHON.md

## Best practices

https://docs.ansible.com/ansible/2.8/user_guide/playbooks_best_practices.html
