CloudWatch Monitoring
=========

This role install the latest AWS CloudWatch monitoring.

Requirements
------------
None

Role Variables
--------------

- `cloud_watch_monitoring_path`: Path where scripts will be installed
- `cron_specs`: {`name`: "Cloudwatch monitoring", `minute`: "*/5", `hour`: "*", `job`: "{{cloud_watch_monitoring_path}}/aws-scripts-mon/mon-put-instance-data.pl --`disk-space-util` --`disk-path`=/mnt/data --from-cron --`aws-access-key-id`=AWS_KEY --`aws-secret-key`=AWS_SECRET_KEY"}



Example Playbook
----------------

To be documented

License
-------

BSD

Author Information
------------------

Cristian Marquez Russo.

Based on the work done by Amrit Singh
