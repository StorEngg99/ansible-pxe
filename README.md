# ansible-pxe
Ansible Playbook for Configuring Kick start Boot server for OS install .

Background : 
  The idea was to configure kickstart and if the same had to be done via Scripts it would have involved lot of greps/awk's/sed to achive this and Ansible playbooks demostrates how it can be archived quicker & with least effort.

Assumptions:
- The CentOS/Redhat ISO/Image is Mounted on /ISO on a FileServer
- The Servers HTTP hosting the ISO image only hosts HTTP service for this purpose

Usage:

- Clone using : git clone https://github.com/StorEngg99/ansible-pxe.git
- Edit the variables to meet your env requirements 
  - Inventory 
    - Ansible host inventory details which would be hosting DHCP/Kickstart Images
    - pxe_vars.yml 
      -DHCP Configuration IP/Subnet/Router info
      -KS Server info & Hostname of server which will be auto-installed using kickstart
    
    
- Run Playbook: ansible-playbook -i inventory provisioning/playbookpxe.yml


