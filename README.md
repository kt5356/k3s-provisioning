# k3s-provisioning

A repo containing the simple ansible playbooks I created to setup and install [k3s| https://k3s.io] 
on my Raspberry Pi cluster. 

## Prerequisites 
- [Raspberry Pi OS|https://www.raspberrypi.com/software/] installed.
- SSH is enabled on the Pi's.
- [Ansible|https://www.ansible.com] has been installed on your local machine.

## Run order
The playbooks should be run in the following order.
- setup.yaml
- cluster.yaml
- cleanup.yaml

The basic command for running a playbook is:
```
ansible-playbook <playbook-name> -u <username> --ask-become-pass --ask-pass
```
For the `setup.yaml` playbook, the `pi` username should be used. The other playbooks 
should be run with the username created in setup. 
If you're using SSH keys, the `--ask-pass` flag can be omited.