Hardening for the new VM deployed:

    1. Update the hosts inventory file with the new VM IP

    2. Enable ssh on the remote host to run the playbook
#ssh-copy-id -i /root/.ssh/id_rsa.pub centos@<new vm ip address>

    3. Run the ansible playbook on the new create centos server from Ubuntu server
#ansible all -m ping --ask-become-pass -u centos
#ansible-playbook -i hosts playbook.yml 
