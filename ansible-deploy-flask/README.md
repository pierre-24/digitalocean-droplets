Ansible playbooks to deploy flask apps.

Assume ubuntu 24.04.

## Setup

A first playbook sets up Python & NGINX:

```bash
ansible-playbook -i hosts install_base.yml -K
```

`-K` is used to request for BECOME password.

## Deploy an app

An example is provided [here](deploy_test.yml):

```bash
ansible-playbook -i hosts deploy_test.yml -K
```

Variables are defined [here](group_vars/all.yml) and should be changed to deploy an app.

## Note: roles

For the general setup:

- [`apt_install`](./roles/apt_install): like its name suggests, ensure that all packages are installed.
- [`nginx_setup`](./roles/nginx_setup): sets up NGINX (thanks to files provided by [nginxconfig.io](https://www.digitalocean.com/community/tools/nginx)).

For the deployment of an app:

- [`app_clone_setup_update`](./roles/app_clone_setup_update): create the directory structure, clone app (or pull the latest version), install requirements (or update them).
- [`service_create_launch`](./roles/services_create_launch): create the services for the app, and for [goaccess](https://goaccess.io/).
- [`nginx_site_setup`](./roles/nginx_site_setup): set up the NGINX to serve the app, 
