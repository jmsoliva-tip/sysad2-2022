## How to create an ansible configuration
1. ANSIBLE_CONFIG (environment variable if set)
2. ansible.cfg (in the current directory)
3. ~/.ansible.cfg (in the home directory)
4. /etc/ansible/ansible.cfg

## How to create an ansible inventory
- You can create your inventory file in one of many formats, depending on the inventory plugins you have. The most common formats are INI and YAML. A basic INI /etc/ansible/hosts might look like this:
- mail.example.com
- [webservers]
- foo.example.com
- bar.example.com

- [dbservers]
- one.example.com
- two.example.com
- three.example.com

## How to create an Ad-hoc Ansible command with setup and shell module.
- $ ssh-agent bash 
- $ ssh-add ~/.ssh/id_rsa 
- $ Ansible abc -a "/sbin/reboot" -f 12
- $ Ansible abc -a "/sbin/reboot" -f 12 -u username
- $ Ansible abc -m copy -a "src = /etc/yum.conf dest = /tmp/yum.conf"
- $ Ansible abc -m file -a "dest = /path/user1/new mode = 777 owner = user1 group = user1 state = directory" 
- $ Ansible abc -m file -a "dest = /path/user1/new state = absent"
- $ Ansible abc -m yum -a "name = demo-tomcat-1 state = present"
- $ Ansible abc -m yum -a "name = demo-tomcat-1 state = absent" 
- $ Ansible abc -m yum -a "name = demo-tomcat-1 state = latest" 
- $ Ansible all -m setup 
