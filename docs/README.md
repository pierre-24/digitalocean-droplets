This is a bit of doc.

# Getting started

I used <https://docs.digitalocean.com/products/droplets/getting-started/recommended-droplet-setup/>

I set up a firewall at <https://cloud.digitalocean.com/networking/firewalls>, with extra HTTP and HTTPS inbound rules.


# Goacess ports

Server `main`

| Service      | Port | Source                                                                                      |
|--------------|------|---------------------------------------------------------------------------------------------|
| `cp2k_basis` | 7201 | [ansible-deploy-flask/deploy_cp2k_basis.yml](../ansible-deploy-flask/deploy_cp2k_basis.yml) |
| `pics`       | 7202 | [ansible-deploy-pics/playbook.yml](../ansible-deploy-pics/playbook.yml)                     |
 

Server `amn`

| Service | Port | Source                                                   |
|---------|------|----------------------------------------------------------|
| `amn`   | 7200 | [ansible-deploy-flask/deploy_amn.yml](../ansible-deploy-flask/deploy_amn.yml) |
 