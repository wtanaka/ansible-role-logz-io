[![Build Status](https://travis-ci.org/wtanaka/ansible-role-logz-io.svg?branch=master)](https://travis-ci.org/wtanaka/ansible-role-logz-io)
[![CircleCI](https://circleci.com/gh/wtanaka/ansible-role-logz-io.svg?style=svg)](https://circleci.com/gh/wtanaka/ansible-role-logz-io)

wtanaka.logz_io
===============

This ansible role installs log shipper configuration for logz_io

Example Playbook
----------------

    - hosts: all
      roles:
         - role: wtanaka.logz_io
           # Get this from
           # https://app.logz.io/#/dashboard/data-sources/rsyslog
           logz_io_secret_key: WojImBeteuWraibutOshpeujdukpeoja
           logz_io_site_config:
             # Conf files get put in
             # /etc/rsyslog.d/21-logzio-{{conf_filename}}.conf
             - conf_filename: nginxerror
               input_file_name: /var/log/nginx/error.log
             # See support.logz.io/support/solutions/articles/6000110550
               input_file_type: nginx-error

License
-------

GPLv2

Author Information
------------------

http://wtanaka.com/
