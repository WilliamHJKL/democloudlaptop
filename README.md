# DEMO CLOUD LAPTOP

The goal of this roles is to deploy a demo plateform on a laptop. For the momemt it deploy network, storage and one vm. You need a ftp server running on your laptop, this ftp server need to share a RHEL7.3 iso.

Configure variables in **group_vars/all** or in **roles/name/vars/main.yml**.

Run as a user the following command (the user need to have correct authorization in sudo). :

```
  ansible-playbook -k --ask-become-pass -i hosts site.yml  --extra-vars "rhn_activationkey=putyouractivationkeyhere rhn_orgid=andyourorgid"
```

The logic behind these playbooks is :

- roles/deploy-infra :

  - configure nested virtualization.
  - install packages for virtualization.
  - create networks :

    - one external network.
    - one internal network.

  - configure storage pool.

- roles/deploy-vms :

  - deploy a number of vms.

- roles/common :

  - configure system's fqdn.
  - register system's in RHN.
  - configure minimal repositories.
  - configure a minimal firewall.

## FIXME

- cleanup.yml : fix know_hosts
- configure-idm : use with_items for sysctl stuff

## TODO

- Optimize VM deployement.
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

- Fix kickstart to use {{ ipaserver_admin_password }}

- Fix kickstart to disable chronyd --force-ntpd

- Fix ipa-client registration.

## LATER

Wait for <https://github.com/ansible/ansible-modules-extras/pull/3247>
