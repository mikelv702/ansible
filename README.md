# Ansible

## Set up
1. Export Digital Ocean PAT
```
export DO_API_TOKEN=<DIGITALOCEAN_PERSONAL_ACCESS_TOKEN>
export DO_SSH_USER=<SSH User>
export DO_SSH_KEY=<SSH Key Path>
export TAILSCALE_KEY=<TAILSCALE API KEY>
```


## Securing hosts

```
ansible-playbook -i inventory/digitalocean.yaml playbooks/fail2ban.yaml -u $DO_SSH_USER --private-key $DO_SSH_KEY

ansible-playbook -i inventory/digitalocean.yaml playbooks/tailscale.yaml -u $DO_SSH_USER --private-key $DO_SSH_KEY
```