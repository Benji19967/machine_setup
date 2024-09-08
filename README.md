# Ansible

## Best practices

https://docs.ansible.com/ansible/2.8/user_guide/playbooks_best_practices.html

## Running a playbook

```bash
HOMEBREW_NO_AUTO_UPDATE=1 ansible-playbook -i inventory site.yml -c local
```

`-c local` tells Ansible not to try to connect through ssh but rather run the playbook 
(site.yml) locally.
