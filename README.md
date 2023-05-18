### This script does the following
- Adds repository and key
- Installs tailscale
- Starts and enables systemd service
- Checks if tailscale is connected
- Bring up tailscale and authinticate to server

Playbook example:
```
- name: ubuntu_servers
  hosts: all
  roles:
    - role: ubuntu_tailscale_deploy
```
If you are not familiar with Ansible, please continue reading. In order to properly execute the playbook example, it should be located one directory above the "ubuntu_tailscale_deploy" directory. Additionally, within the same directory as the playbook, you will need to include an "inventory.yml" file  
Inventory example:
```
ubuntu_servers:
  hosts:
    email:
      ansible_host: 172.16.3.22
```