Ansible playbooks to setup droplets.

Assume ubuntu 24.04.

## Run

```bash
ansible-playbook -i hosts playbook.yml -J
```

## Note: roles

- [`apt_install`](../ansible-general-setup/roles/apt_install): like its name suggests, ensure that all packages are installed.
- [`nginx_setup`](../ansible-general-setup/roles/nginx_setup): sets up NGINX (thanks to files provided by [nginxconfig.io](https://www.digitalocean.com/community/tools/nginx)).