# DEMO CLOUD LAPTOP

The goal of this roles is to deploy a demo plateform on a laptop. For the momemt it deploy network, storage and one vm. You need a ftp server running on your laptop, this ftp server need to share a RHEL7.3 iso.

Configure variables in **group_vars/all** or in **roles/name/vars/main.yml**.

Run as a user the following command (the user need to have correct authorization in sudo). :

```

  ansible-playbook -k --ask-become-pass -i inventory site.yml  --extra-vars "rhn_activationkey=putyouractivationkeyhere rhn_orgid=andyourorgid"
```

The logic behind these playbooks is:

**roles/_deploy-infra:_**

- configure nested virtualization.
- install packages for virtualization.
- create networks:

  - one external network.
  - one internal network.

- configure storage pool.

**roles/_deploy-vms:_**

- deploy a number of vms.

**roles/_common:_**

- configure system's fqdn.
- register system's in RHN.
- deactivate ipv6
- configure a minimal firewall.
- configure minimal repositories.

**roles/_configure-idm_**

- configure idm.

**roles/_configure-host_**

- a quick and dirty hack to get dns resolution working from kvm host.

**roles/_cleanup_**

- the beginning of a cleanup playbooks, once writen it will desinstalle everything ...

## LATER

Wait for <https://github.com/ansible/ansible-modules-extras/pull/3247>
