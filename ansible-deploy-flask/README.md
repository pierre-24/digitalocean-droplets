Ansible playbooks to deploy flask apps.

Assume debian/ubuntu

## Setup

Create an `inventory` file.

A first playbook sets up Python & NGINX:

```bash
ansible-playbook -i inventory install_base.yml -K
```

`-K` is used to request for BECOME password.

You might want to [use the official `goaccess` repo](https://goaccess.io/download#official-repo) to get up to date version.

## Deploy an app

An example is provided [here](deploy_test.yml):

```bash
ansible-playbook -i inventory deploy_test.yml -K
```

Variables are defined [here](group_vars/all.yml) and can be changed to deploy another app.

## TODO

- [ ] [goaccess](https://goaccess.io/)? (with `.htpasswd`, maybe? :p )
