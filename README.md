# democloudlaptop :
- The goal of this roles is to deploy a demo plateform on a laptop. For the momemt it deploy network, storage and one vm. You need a ftp server running on your laptop.
- Run ansible-playbook -k --ask-become-pass -i hosts site.yml as a simple user. The user need to have correct authorization in sudo.
# TODO :
- Configure IPA : WIP
- Configure host to use the idm for dns resolution on zone $dns_name
- - > /etc/NetworkManager/dnsmasq.d
- - > server=/example.demo/172.31.0.254
- - > server=/31.172.in-addr.arpa./172.31.0.254
- Deploy Satellite
- Configure Satellite.
# DONE :
- Deploy infra : network / storage / vm.
# FIXME :
# LATER :
Wait for https://github.com/ansible/ansible-modules-extras/pull/3247
