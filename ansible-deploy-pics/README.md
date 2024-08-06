Ansible playbooks to deploy <https://github.com/pierre-24/pics.pierrebeaujean.net>

Assume ubuntu 24.04.

## Run

```bash
ansible-playbook -i hosts playbook.yml -J
```

## Note: roles

- [`gallery_init_setup`](./roles/gallery_init_setup): create directory structure, install package.
- [`gallery_update`](./roles/gallery_update): upload images and make site.