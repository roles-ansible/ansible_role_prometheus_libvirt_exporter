 ansible_role_prometheus-libvirt-exporter
==========================================

[![galaxy](https://raw.githubusercontent.com/roles-ansible/ansible_role_prometheus-libvirt-exporter/main/.github/galaxy.svg)](https://galaxy.ansible.com/do1jlr/prometheus_libvirt_exporter)
[![license](https://raw.githubusercontent.com/roles-ansible/ansible_role_prometheus-libvirt-exporter/main/.github/license.svg)](https://github.com/roles-ansible/ansible_role_prometheus-libvirt-exporter/blob/main/LICENSE)

Ansible role to install the golang prometheus node exporter from [github.com/zhangjianweibj/prometheus-libvirt-exporter](https://github.com/zhangjianweibj/prometheus-libvirt-exporter.git).

 What does this role do?
-------------------------
First we download the latest release from the [prometheus-libvirt-exporter](https://github.com/zhangjianweibj/prometheus-libvirt-exporter.git) Releases. Obviously we extract it and create a symlink to the binary go executable to /usr/local/bin/.
Then we install, start and enable a systemd service that will run the /usr/local/bin/prometheus-libvirt-exporter binary.

 Variables:
---------------
Have a look into defauts/main.yml for a full list.
+ the ``prometheus_libvirt_exporter__version`` variable defines the Released version tis role will install.
+ the ``prometheus_libvirt_exporter__repo`` is pointing to the ``https://github.com/zhangjianweibj/prometheus-libvirt-exporter`` Repo.
+ If you set ``submodules_versioncheck`` to ``true`` we try to prevent running a old version of this role at your deployed hosts.

