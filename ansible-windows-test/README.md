# using ansible-windows-test

## In long:
Follow the following article to know the whole deal surrounding Windows and Ansible. Configure as necessary for your environment and claim to be omnipotent about Windows integration, otherwise known as *Ansible on Hard Mode* (tm).
* https://docs.ansible.com/ansible/latest/intro_windows.html

## In short:

#### prepare your target system
* https://docs.ansible.com/ansible/latest/intro_windows.html#windows-system-prep

#### on windows subsystem for linux
```sudo apt-get update
sudo apt-get install python-pip git libffi-dev libssl-dev -y
pip install ansible pywinrm
```

#### on linux
```
sudo add-apt-repository ppa:ansible/ansible
sudo apt-get install ansible -y
```

then,

0. clone this
1. edit and move hosts into `/etc/ansible/hosts` or make the appropriate config to reference it in the local dir
2. edit `group_vars\windows.yml` to contain the proper user/pass combo
3. `ansible-playbook main.yml`
