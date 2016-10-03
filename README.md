Init
====

[![Build Status](https://travis-ci.org/jebovic/ansible-init.svg?branch=master)](https://travis-ci.org/jebovic/ansible-init) [![Ansible Galaxy](https://img.shields.io/badge/galaxy-jebovic.init-blue.svg?style=flat)](https://galaxy.ansible.com/jebovic/init)

Default init role for needed stuff on all servers

Role Variables
--------------

```
# Pip configuration
pip_download_url: https://bootstrap.pypa.io/get-pip.py
pip_download_dest: /tmp
pip_version: latest
python: python
pip: pip

# Default apt packages to install
init_apt_packages:
  - vim
  - curl
  - wget
  - htop
  - ntp
  - logrotate
  - unzip
  - sendmail-bin
  - sendmail

# Default pip packages to install
init_pip_packages:
  - httpie

# /etc/hosts configuration
custom_hosts: []

# ntp basic configuration
ntp_servers:
  - 0.fr.pool.ntp.org
  - 1.fr.pool.ntp.org
  - 2.fr.pool.ntp.org
  - 3.fr.pool.ntp.org

# timezone configuration
timezone_name: Europe/Paris
```

Example Playbook
----------------

```
    - hosts: servers
      roles:
         - { role: jebovic.init }
```

License
-------

MIT

Author Information
------------------

Jérémy Baumgarth https://github.com/jebovic
