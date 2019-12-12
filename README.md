raspi-ddns-update
=========

Installs a script (and associated systemd startup files) to send periodic
updates of one's external NAT address to an authoritative DNS server via
RFC 2845 compatible TSIG-authenticated update messages

Requirements
------------

none

Role Variables
--------------

These variables will be self-explanitory to anyone who is familiar with RFC 2845 style updates.
Probably best to set these in {{ inventory_dir }}/host_vars/hostname.yml

ddns_update_server: "192.0.2.53"

ddns_update_hostname: "foo.dyn.example.org"

ddns_update_keyname: "testhost.example.org-20190304-00"
ddns_update_keyhmac: "MguqAW/Ea33RhBNF1CKDvRMc07EelaKS3FumqmathE4="



for your requirements.yml:

- src: https://github.com/res3066/ansiblerole-raspi-ddns-update
  name: raspi-ddns-update
  scm: git


Dependencies
------------

none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - raspi-ddns-update

License
-------

MIT

Author Information
------------------

Rob Seastrom <rs@seastrom.com>

