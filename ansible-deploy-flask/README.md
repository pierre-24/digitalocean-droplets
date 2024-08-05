Ansible playbooks to deploy flask apps.

Assume ubuntu 24.04.

## Use

An example is provided [here](deploy_test.yml):

```bash
ansible-playbook -i hosts deploy_test.yml -J
```

Variables are defined [here](group_vars/all.yml) and should be changed to deploy an app.

## Note: roles

- [`app_clone_setup_update`](./roles/app_clone_setup_update): create the directory structure, clone app (or pull the latest version), install requirements (or update them).
- [`service_create_launch`](./roles/services_create_launch): create the services for the app, and for [goaccess](https://goaccess.io/).
- [`nginx_site_setup`](./roles/nginx_site_setup): set up the NGINX to serve the app.
