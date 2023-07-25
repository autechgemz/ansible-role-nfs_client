# Ansible Role: nfs_client

## Description

Manage nfs client configration and mounts.

## Requirements

None

## Dependencies

None

## OS Platforms

- RHEL-7/CentOS-7 or higher
- Ubuntu-20.04 or higher
- AlmaLinux-8 or higher
- Rockylinux-8 or higher

## Example Playbook

```
- hosts: all
  roles:
    - nfs_client
```

## Role variables

### nfs_client_package_ensure: (string)

```
nfs_client_package_ensure: 'present'
```

### nfs_client_service_ensure: (string)

```
nfs_client_service_ensure: 'started'
```

### nfs_client_service_enable: (bool)

```
nfs_client_service_enable: true
```

### nfs_client_mounts: (list)

```
nfs_client_mounts: []
```

### nfs_client_daemon_config_options: (dict)

```
nfs_client_daemon_config_options: {}
```

### nfs_client_config_options: (dict)

```
nfs_client_config_options: {}
```

### nfs_client_dropin_config_purge: (bool)

```
nfs_client_dropin_config_purge: false
```

### nfs_client_dropin_config_options: (dict)

```
nfs_client_dropin_config_options: {}
```

## Example vars

```
nfs_client_mounts:
  - { path: '/mnt/home', server: '192.168.56.101', device: '/export/home' }

or

nfs_client_mounts:
  - { path: /mnt/home, server: 192.168.56.101, device: /export/home, fstype: nfs, options: 'nfsvers=3,tcp,rw,hard,bg,intr', state: mounted }
```
