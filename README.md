vmware_vm_resize
=========

Resize VMware VM vCPU and Memory

Requirements
------------


Role Variables
--------------

| Role variable name | Description |
| ------------------ | ------------------ |
| vmware_vm_resize_hostname | vCenter hostname |
| vmware_vm_resize_username | vCenter username |
| vmware_vm_resize_password | vCenter password |
| vmware_vm_resize_validate_certs | true or false (default) |
| vmware_vm_resize_datacenter | vCenter datacenter |
| vmware_vm_resize_vm_folder | vCenter folder |
| vmware_vm_resize_vm_name | vCenter VM name (when vm uuid is not provided) |
| vmware_vm_resize_vm_uuid | vCenter VM uuid (when vm name is not provided) |
| vmware_vm_resize_num_cpus | vCenter VM number of vCPU |
| vmware_vm_resize_memory_mb | vCenter VM memory size in MB |
| vmware_vm_resize_no_reboot | true (default) - don't restart the vm to make change <br> false - shutdown and restart vm to make change |



Dependencies
------------


Example Playbook
----------------
```yaml
  - name: Resize VM
    import_role:
      name: vmware_vm_resize
    vars:
      vmware_vm_resize_hostname: vcenter.lab.home
      vmware_vm_resize_username: admin@lab.home
      vmware_vm_resize_password: admin_password
      vmware_vm_resize_validate_certs: false
      vmware_vm_resize_datacenter: "Prod Datacenter"
      vmware_vm_resize_vm_folder: "Folder1/Folder2"
#      vmware_vm_resize_vm_name: my_vm
      vmware_vm_resize_vm_uuid: 42204ef7-04c2-571e-eada-26ade77cfc95
      vmware_vm_resize_num_cpus: 2
      vmware_vm_resize_memory_mb: 4096
      vmware_vm_resize_no_reboot: false
```

License
-------

BSD

Author Information
------------------

Eric Chong (echong@redhat.com)
