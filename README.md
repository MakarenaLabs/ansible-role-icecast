<p align="center">
  <img src="https://gitlab.xiph.org/uploads/-/system/project/avatar/2/240px-Icecast-Logo-Alternative.svg.png">
</p>

# Ansible Role: Icecast
[![Build Status](https://travis-ci.org/MakarenaLabs/ansible-role-icecast.svg?branch=master)](https://travis-ci.org/MakarenaLabs/ansible-role-icecast)
[![License](https://img.shields.io/github/license/MakarenaLabs/ansible-role-icecast.svg)](https://opensource.org/licenses/MIT)
[![Ansible Version](https://img.shields.io/badge/ansible-%3E%3D_1.4-8892BF.svg)](https://www.ansible.com/)
[![Ansible Role](https://img.shields.io/ansible/role/36514.svg)](https://galaxy.ansible.com/MakarenaLabs/icecast/)
[![Ansible Quality](https://img.shields.io/ansible/quality/36514.svg)](https://galaxy.ansible.com/MakarenaLabs/icecast/)
[![Ansible Downloads](https://img.shields.io/ansible/role/d/36514.svg)](https://galaxy.ansible.com/MakarenaLabs/icecast/)

Ansible role that installs Icecast for your personal media streaming.

## Installation

Using `ansible-galaxy`:
```shell
$ ansible-galaxy install makarenalabs.icecast
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):
```shell
$ arm install makarenalabs.icecast
```

Using `git`:
```shell
$ git clone https://github.com/MakarenaLabs/ansible-role-icecast.git
```

## Requirements & Dependencies
- Ansible 1.4 or higher

## Variables
Here is a list of all the default variables for this role, which are also available in `vars/main.yml`.

```yaml
ice_location: Earth
ice_admin: icemaster@localhost
ice_adminuser: admin
ices2_configfile: "/etc/icecast2/icecast.xml"
ices2_streamname: Example stream name
ices2_genre: Example genre
ices2_description: A short description of your stream
```
  - ```ice_hostname```
  - ```ice_sourcepassword```
  - ```ice_relaypassword```
  - ```ice_adminpassword```

These variables are required!

## Example playbook
```yaml
---
- hosts: all
  vars:
    - ice_hostname: localhost
    - ice_sourcepassword: hackme
    - ice_relaypassword: hackme
    - ice_adminpassword: hackme
    - ice_location: Earth
    - ice_admin: icemaster@localhost
    - ice_adminuser: admin
  roles:
    - makarenalabs.icecast
```

## Testing
```shell
$ git clone https://github.com/MakarenaLabs/ansible-role-icecast.git
$ cd ansible-role-icecast
$ vagrant up
```

## License

Licensed under the MIT License. See the LICENSE file for details.

Copyright © 2019 [MakarenaLabs](https://www.makarenalabs.com)
