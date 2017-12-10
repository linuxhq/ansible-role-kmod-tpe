# ansible-role-kmod-tpe

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-kmod-tpe.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-kmod-tpe)

RHEL/CentOS - Trusted Path Execution Linux Kernel Module

## Requirements

None

## Role Variables

Available variables are listed below, along with default values.

    kmod_tpe_admin_gid: 0
    kmod_tpe_check_file: True
    kmod_tpe_dmz_gid: 0
    kmod_tpe_extras_harden_ptrace: True
    kmod_tpe_extras_hide_uname: False
    kmod_tpe_extras_ignore_softmode: False
    kmod_tpe_extras_log: True
    kmod_tpe_extras_lsmod: True
    kmod_tpe_extras_proc_kallsyms: True
    kmod_tpe_extras_ps: False
    kmod_tpe_extras_ps_gid: 0
    kmod_tpe_extras_restrict_setuid: False
    kmod_tpe_hardcoded_path: []
    kmod_tpe_kernel_dmesg_restrict: False
    kmod_tpe_kernel_modules_disabled: False
    kmod_tpe_kill: False
    kmod_tpe_lock: False
    kmod_tpe_log: True
    kmod_tpe_log_floodburst: 5
    kmod_tpe_log_floodtime: 5
    kmod_tpe_log_max: 50
    kmod_tpe_log_verbose: True
    kmod_tpe_paranoid: False
    kmod_tpe_softmode: False
    kmod_tpe_strict: True
    kmod_tpe_trusted_apps: []
    kmod_tpe_trusted_gid: 0
    kmod_tpe_trusted_invert: False
    kmod_tpe_xattr_soften: True

## Dependencies

 * https://galaxy.ansible.com/linuxhq/elrepo/

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.kmod-tpe
          kmod_tpe_extras_proc_kallsyms: True
          kmod_tpe_extras_ps: True
          kmod_tpe_extras_lsmod: True
          kmod_tpe_extras_restrict_setuid: True
          
## License

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
