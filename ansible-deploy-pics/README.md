Ansible playbooks to deploy <https://github.com/pierre-24/pics.pierrebeaujean.net>

Assume ubuntu 24.04.

## Run

```bash
ansible-playbook -i hosts playbook.yml -J
```

## Note: roles

- [`gallery_init_setup`](./roles/gallery_init_setup): create directory structure, install package, init gallery.
- [`gallery_update`](./roles/gallery_update): upload images and make gallery.
- [`nginx_site_setup`](./roles/nginx_site_setup): : set up NGINX to serve the gallery.