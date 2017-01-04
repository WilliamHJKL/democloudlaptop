# democloudlaptop

- The goal of this roles is to deploy a demo plateform on a laptop. For
the momemt it deploy network, storage and one vm. You need a ftp server
running on your laptop, this ftp server will server a RHEL7.3 iso.
- Configure variables in **group_vars/all** or in **roles/name/vars/main.yml**.
- Run :
```
ansible-playbook -k --ask-become-pass -i hosts site.yml
```
as a simple user. The user need to have correct authorization in sudo.

## FIXME
- Add vars_prompt for all roles.
- Fix kickstart to use {{ ipaserver_admin_password }}
- Fix kickstart to disable chronyd --force-ntpd

## TODO
- - generic kickstart
- - variables in site.yml like :
  ---
  - role: deploy_generic_vm
    vm_name: XXX
    system_disk_size: 8
    mem_size: 2048
    num_cpus: 2
- Configure Satellite.

## DONE

- Deploy infra : network / storage / vm.
- Deploy vm IDM
- Configure IDM
- Deploy Satellite
- Configure repository
- Fix masquerading.
- Create a common for rhn registration / basic firewall (ssh) / basic repositories subscription
- - Register in RHN
- Move deploy-vm-blank to deploy-vm-generic
- Register in IPA (done via kickstart)

## FIXME

## LATER
Wait for https://github.com/ansible/ansible-modules-extras/pull/3247
