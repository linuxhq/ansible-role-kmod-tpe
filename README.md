# ansible-role-kmod-tpe

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-kmod-tpe.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-kmod-tpe)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-kmod--tpe-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/kmod-tpe)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

RHEL/CentOS - Trusted Path Execution Linux Kernel Module

## Requirements

This role requires that you have the elrepo repository installed.

 * https://galaxy.ansible.com/linuxhq/elrepo/

## Role Variables

Available variables are listed below, along with default values.

    kmod_tpe_admin_gid: 0
    kmod_tpe_check_file: true
    kmod_tpe_dmz_gid: 0
    kmod_tpe_extras_harden_ptrace: true
    kmod_tpe_extras_hide_uname: false
    kmod_tpe_extras_ignore_softmode: false
    kmod_tpe_extras_log: true
    kmod_tpe_extras_lsmod: true
    kmod_tpe_extras_proc_kallsyms: true
    kmod_tpe_extras_ps: false
    kmod_tpe_extras_ps_gid: 0
    kmod_tpe_extras_restrict_setuid: false
    kmod_tpe_hardcoded_path: []
    kmod_tpe_kernel_dmesg_restrict: false
    kmod_tpe_kernel_modules_disabled: false
    kmod_tpe_kill: false
    kmod_tpe_lock: false
    kmod_tpe_log: true
    kmod_tpe_log_floodburst: 5
    kmod_tpe_log_floodtime: 5
    kmod_tpe_log_max: 50
    kmod_tpe_log_verbose: true
    kmod_tpe_paranoid: false
    kmod_tpe_softmode: false
    kmod_tpe_strict: true
    kmod_tpe_trusted_apps: []
    kmod_tpe_trusted_gid: 0
    kmod_tpe_trusted_invert: false
    kmod_tpe_xattr_soften: true

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.kmod-tpe
          kmod_tpe_extras_proc_kallsyms: true
          kmod_tpe_extras_ps: true
          kmod_tpe_extras_lsmod: true
          kmod_tpe_extras_restrict_setuid: true
          
## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
