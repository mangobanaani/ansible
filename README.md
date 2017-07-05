# ansible
Ansible playbooks

ansible_updates.yml - updates Linux servers (Debian/RHEL/OSX(Homebrew)) as needed, including autoclean and reboots

after you have your servers in /etc/ansible/hosts in form 
<pre>
[testing_servers]
web1
web2
web3
[testing_servers:vars]
ansible_ssh_user=sshuser
ansible_ssh_pass=sshuser
</pre>
execute playbooks against group of servers for example by 
<pre>
ansible-playbook testing_servers ansible_updates.yml --ask-become -v
</pre>

