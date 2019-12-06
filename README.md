Python Docker SDK role for Ansible
=================

A simple role for installing the [Python Docker SDK](https://docker-py.readthedocs.io/en/stable/) on your APT-enabled hosts using [Ansible](http://www.ansibleworks.com/). This ensures Ansible's docker modules will operate on your hosts.

Usage
-----

This role uses [APT](https://docs.ansible.com/ansible/latest/modules/apt_module.html) to ensure the required packages on your hosts. Any other package manager is not supported for now.

Clone this repo into your roles directory:

    $ git clone https://github.com/emielmolenaar/ansible-role-docker-python-sdk.git roles/docker-python-sdk

And add it to your play's roles:

    - hosts: ...
      roles:
        - docker-python-sdk
        - ...

I recommend using a `requirements.yml` in your roles directory though:

    - src: https://github.com/emielmolenaar/ansible-role-docker-python-sdk.git
      name: docker-python-sdk

Installing the role will require a `ansible-galaxy install -r ./roles/requirements.yml -p ./roles` from the root directory of your playbook.
