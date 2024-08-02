Ansible playbooks to deploy flask apps.

## Setup

Create an `inventory` file.

A first playbook sets up Python & NGINX:

```bash
ansible-playbook -i inventory install_base.yml -K
```

`-K` is used to request for BECOME password.

## Deploy an app

An example is provided [here](deploy_test.yml):

```bash
ansible-playbook -i inventory deploy_test.yml -K
```

Variables are defined [here](group_vars/all) and can be changed to deploy another app.

## TODO

- [ ] logrotate?