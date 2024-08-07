Ansible playbooks to setup droplets.

Assume ubuntu 24.04.

## Run

```bash
ansible-playbook -i hosts playbook.yml -J
```

## Note: roles

Inspired in part by [`ansible-zestedesavoir`](https://github.com/zestedesavoir/ansible-zestedesavoir).

- [`apt_install`](./roles/apt_install): like its name suggests, ensure that all packages are installed.
- [`droplet_setup`](./roles/droplet_setup): setup a few variables on the remote.
- [`nginx_setup`](./roles/nginx_setup): sets up NGINX (thanks to files provided by [nginxconfig.io](https://www.digitalocean.com/community/tools/nginx)).