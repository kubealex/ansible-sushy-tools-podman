ansible-sushy-tools-podman
=========

This role allow the setup of a sushy-tools emulation instance to use libvirt as the underlying layer for BMC.

Requirements
------------

The role requires the collection **community.crypto**, the python library **cryptography** and **podman** to be present.

Role Variables
--------------

The role can be configured to have a predefined username and password for BMC credentials, as well as the port where it will be listening.

    sushy_host: 0.0.0.0
    sushy_port: 8000
    sushy_admin_user: admin
    sushy_admin_password: redhat


Example Playbook
----------------

Use this requirements.yml to setup your dependencies:

    ---
    collections:
      - community.crypto
      - community.general
    roles:
      - name: ansible-sushy-tools-podman
        src: https://github.com/kubealex/ansible-sushy-tools-podman.git

Sample usage with default settings:

    - hosts: podman_host
      roles:
        - ansible-sushy-tools-podman

License
-------

BSD
