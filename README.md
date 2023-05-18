### This script does the following
- Adds repository and key
- Installs tailscale
- Starts and enables systemd service
- Checks if tailscale is connected
- Bring up tailscale and authinticate to server

Playbook example
```
- name: ubuntu_servers
  hosts: all
  roles:
    - role: ubuntu_tailscale_deploy
```
If you have not used Ansible a lot keep reading.  
for the playbook example it will need to be one directory up from the ubuntu_tailscale_deploy directory.
Also in the same directory as the playbook you will need an inventory.yml that looks something like this.
```
ubuntu_servers:
  hosts:
    email:
      ansible_host: 172.16.3.22
```
Notice that the same name is used at the top of the playbook as is used in the invintory.yml ubuntu_servers. 