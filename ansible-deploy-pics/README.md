Ansible playbooks to deploy <https://github.com/pierre-24/pics.pierrebeaujean.net>

Assume ubuntu 24.04.

## Run

```bash
ansible-playbook -i hosts playbook.yml -J
```

## Note: roles

- [`app_setup`](../ansible-general-setup/roles/apt_install): clone repository, create directory structure.
- [`nginx_setup`](../ansible-general-setup/roles/nginx_setup): sets up NGINX (thanks to files provided by [nginxconfig.io](https://www.digitalocean.com/community/tools/nginx)).