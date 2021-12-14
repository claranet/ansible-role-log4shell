# Ansible role - log4shell
[![Maintainer](https://img.shields.io/badge/maintained%20by-claranet-e00000?style=flat-square)](https://www.claranet.fr/)
[![License](https://img.shields.io/github/license/claranet/ansible-role-log4shell?style=flat-square)](LICENSE)
[![Release](https://img.shields.io/github/v/release/claranet/ansible-role-log4shell?style=flat-square)](https://github.com/claranet/ansible-role-log4shell/releases)
[![Status](https://img.shields.io/github/workflow/status/claranet/ansible-role-log4shell/Ansible%20Molecule?style=flat-square&label=tests)](https://github.com/claranet/ansible-role-log4shell/actions?query=workflow%3A%22Ansible+Molecule%22)
[![Ansible version](https://img.shields.io/badge/ansible-%3E%3D2.10-black.svg?style=flat-square&logo=ansible)](https://github.com/ansible/ansible)
[![Ansible Galaxy](https://img.shields.io/badge/ansible-galaxy-black.svg?style=flat-square&logo=ansible)](https://galaxy.ansible.com/claranet/log4shell)


> :star: Star us on GitHub — it motivates us a lot!

Find Log4Shell CVE-2021-44228 on your system

This role tries to find jar and war from filesystem and from opened files (lsof)

:warning: Your system may runs slowly during the scan

This role populates the variable `log4shell_analyze_versions` with a dictionary like this one: `{"/tmp/rundeck.war": "2.13.2",}`.
The key is the path where the role has found the log4j library and the value is the log4j's version.

## :warning: Requirements

Ansible >= 4

## :zap: Installation

```bash
ansible-galaxy install claranet.log4shell
```

## :gear: Role variables

Variable                | Default value | Description
------------------------|---------------|------------------------
log4shell_scan_path     | /             | Filesystem path to scan

## :arrows_counterclockwise: Dependencies

N/A

## :pencil2: Example Playbook

```yaml
---
- hosts: all
  roles:
    - role: claranet.log4shell
      log4shell_scan_path: /opt
```

## :closed_lock_with_key: [Hardening](HARDENING.md)

## :heart_eyes_cat: [Contributing](CONTRIBUTING.md)

## :copyright: [License](LICENSE)

[Mozilla Public License Version 2.0](https://www.mozilla.org/en-US/MPL/2.0/)
