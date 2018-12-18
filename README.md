# GAP
This set up GAP stack in openshift via ansible run , the playbooks were taken from openshift-ansible and customised a little.


###Runing it
This playbook depends on the various facts obtained from openshift-ansible, hence we need to set the ANSIBLE_ROLES_PATH.
Also we need to make sure we have the inventory file. Its ideal to be used for the openshift installations where we have everything ready, ie openshift-ansible installed
and the related inventory file that was used for cluster provisioning.

Various vars in the playbooks are passed via file in vars directory.

```
ANSIBLE_ROLES_PATH=${DEFAULT_ROLES_PATH}:/usr/share/ansible/openshift-ansible/roles ansible-playbook -i inventory/hosts setup-prometheus-grafana.yml
```
