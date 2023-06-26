Jenkins CI Cluster
=========

Role for installing Jenkins Farm with agents via Docker-Compose

Requirements
------------

Required docker installation and\or docker role.

Role Variables
--------------

**jenkins_agent_1_secret** - secret for connecting to main cluster for agent 1
**jenkins_agent_2_secret** - secret for connecting to main cluster for agent 2
**jenkins_archive_password** - password from tarball

Dependencies
------------

Infrastructure under galaxy.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
