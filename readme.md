Papertrail Role
===================

This role sets up papertrail on the host the playbook runs, on, setting up logging via TLS to a host and port defined by `papertrail_logging_host` and `papertrail_logging_port`.

Right now, it works with remote_syslog over TLS, and rsyslog over UDP, but frustratingly, not rsyslog over TLS.




Usage
==============

1. Download this role, and place it in your roles directory.
2. Update the `papertrail_logging_host` and `papertrail_logging_port` vars to the ones supplied on the Papertrail WebUI
3. Add role to your playbook


```yml
vars:
  - papertrail_logging_host: logs2.papertrailapp.com
  - papertrail_logging_port: 51234

roles:
 - productscience.papertrailapp
```
