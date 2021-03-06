Ansible Papertrail Role
=========

Role for configuring papertrail service. 
Currently only rsyslog is supported and confirmed to be working on Debian like systems

Requirements
------------

- Rsyslogd should already be installed.
- `papertrail_destination` should be configured

Role Variables
--------------

- `papertrail_destination`: Papertrail Destination host:port i.e. logs1234.papertrailapp.com:1234
- `papertrail_enable_tcp`: Enable TCP connection. Default: False
- `papertrail_enable_tls:`: Enable TLS. Only works with TCP. Default: True
- `papertrail_loglevel`: loglevel. Default: \*.\*
- `papertrail_hostname`: Hostname to send logs from. Default: System hostname

Rsyslog Defaults
----------------

- `papertrail_EscapeControlCharactersOnReceive`. Default (string): 'on'

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: alekseyp.papertrail, papertrail_destination: logs1234.papertrailapp.com:1234}


TODO
-------

Add support for 

- syslog
- syslog-ng
- other OSs



License
-------

MIT

Author Information
------------------

Aleksey Potaneyko

Mediahub