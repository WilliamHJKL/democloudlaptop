# democloudlaptop :
- Run ansible-playbook -v --ask-become-pass -i hosts site.yml as a simple user. The user need to have correct authorization in sudo.
- The role deploy-kvm-vm deploy a vm based on a template. (a simple RHEL 7.2). It's just there for testing purpose.
# TODO :
- Adapt deploy-kvm-vm to deploy using virt-install.
# FIXME :


# LATER :
Wait for https://github.com/ansible/ansible-modules-extras/pull/3247
