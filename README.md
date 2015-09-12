# Test

This playbook is to test `debops.nginx` http and https site detection.

## Dependencies

1. https://www.vagrantup.com/
1. http://www.ansible.com/

## Install

1. `mkdir test && git clone https://github.com/patrickheeney/ansible-nginx-test.git test && cd test`
1. `git clone https://github.com/protobox/protobox.git vendor/protobox`
1. `ansible-galaxy install -f -r requirements.yml -p vendor/roles`
1. `vagrant up`

## Test

1. `ansible-playbook -i hosts playbooks/vagrant.yml`
1. `ansible-playbook -i hosts playbooks/vagrant.yml -t sites`
1. `ansible-playbook -i hosts playbooks/vagrant.yml -t nginx`
