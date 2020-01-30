vmware_vm_resize
=========

Resize VMware VM vCPU and Memory

Requirements
------------


Role Variables
--------------

| vmware_vm_resize_hostname | vCenter URL |
| vmware_vm_resize_username | vCenter username |
| vmware_vm_resize_password | vCenter password |
| vmware_vm_resize_validate_certs | true or false |
| vmware_vm_resize_datacenter | vCenter datacenter |
| vmware_vm_resize_folder | vCenter folder |
| vmware_vm_resize_vm_name | vCenter VM name |
| vmware_vm_resize_num_cpus | vCenter VM number of vCPU |
| vmware_vm_resize_memory_mb | vCenter VM memory size in MB |



Dependencies
------------


Example Playbook
----------------
```yaml
  - name: Resize VM
    import_role:
      name: vmware_vm_resize
    vars:
      vmware_vm_resize_hostname: "{{ vmware_vm_vcenter.hostname }}"
      vmware_vm_resize_username: "{{ vmware_vm_vcenter.username }}"
      vmware_vm_resize_password: "{{ vmware_vm_vcenter.password }}"
      vmware_vm_resize_validate_certs: "{{ vmware_vm_vcenter.validate_certs }}"
      vmware_vm_resize_datacenter: "{{ vmware_vm_vm.datacenter }}"
      vmware_vm_resize_folder: "{{ vmware_vm_vm.folder }}"
      vmware_vm_resize_vm_name: "{{ vmware_vm_vm.name }}"
      vmware_vm_resize_num_cpus: "1"
      vmware_vm_resize_memory_mb: 4096
```

License
-------

BSD

Author Information
------------------

Eric Chong (echong@redhat.com)
