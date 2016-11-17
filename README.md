# democloudlaptop :
- Adjust variables in roles/$rolename/defaults/var.yml if needed. Hint : grep CHANGEME
- Run ansible-playbook -v --ask-become-pass -i hosts site.yml as a simple user. The user need to have correct authorization in sudo.

# TODO :
- Configure dnsmasq and dhcpd for srv.example.demo.
- Configure connection sharing on srv.example.demo.
- Configure ipa on srv.example.demo 

# FIXME :

# LATER :
Wait for https://github.com/ansible/ansible-modules-extras/pull/3247
Find a way to deploy several vm each with a unique name.
