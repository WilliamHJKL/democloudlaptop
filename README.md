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

- Fix masquerading.

## TODO
- Configure Satellite.
- - Register in RHN
- - Register in IPA.
- - Configure repository.

## DONE

- Deploy infra : network / storage / vm.
- Deploy vm IDM
- Configure IDM
- Deploy Satellite
- Configure repository

## FIXME

## LATER
Wait for https://github.com/ansible/ansible-modules-extras/pull/3247
