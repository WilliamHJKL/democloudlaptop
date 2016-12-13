# democloudlaptop :
- The goal of this roles is to deploy a demo plateform on a laptop. For
the momemt it deploy network, storage and one vm. You need a ftp server
running on your laptop.
- Run ansible-playbook -k --ask-become-pass -i hosts site.yml as a
simple user. The user need to have correct authorization in sudo.
# TODO :
- Deploy Satellite
- Configure Satellite.
# DONE :
- Deploy infra : network / storage / vm.
- Deploy vm idm
- Configure IDM
# FIXME :
# LATER :
Wait for https://github.com/ansible/ansible-modules-extras/pull/3247
