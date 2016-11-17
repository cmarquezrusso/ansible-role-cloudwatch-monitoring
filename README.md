ansible-role-cloudwatch-monitoring
=========
[![Build Status](https://travis-ci.org/cristian04/ansible-role-cloudwatch-monitoring.svg?branch=master)](https://travis-ci.org/cristian04/ansible-role-cloudwatch-monitoring)

This role install the latest AWS CloudWatch monitoring.

Tested on Ansible 2.2.0.0

How to
----------------

# Installation

`ansible-galaxy install cristian04.cloudwatch-monitoring`

# Recommendations:
- Don't add the role into Source Control. Use `ansible-galaxy` instead
- You can create a `requirements` file by typing `ansible-galaxy list >> galaxy.roles.yml`
- To install all the `ansible-galaxy` dependencies, execute `ansible-galaxy install -r galaxy.roles.yml`
- Your `ansible.cfg` file must be configured with the correct path to the roles.
- You can override `ansible.cfg` using the `-p` parameter. Example: `ansible-galaxy install -r galaxy.roles.yml -p roles/`  

Role Variables
--------------

- `cloud_watch_monitoring_path`: Path where scripts will be installed
- `cron_specs`: {`name`: "Cloudwatch monitoring", `minute`: "*/5", `hour`: "*", `job`: "{{cloud_watch_monitoring_path}}/aws-scripts-mon/mon-put-instance-data.pl --`disk-space-util` --`disk-path`=/mnt/data --from-cron --`aws-access-key-id`=AWS_KEY --`aws-secret-key`=AWS_SECRET_KEY"}
- 
# TODOs

- [ ] Add tests
- [ ] Add Vagrant images to test


License
-------

BSD

Author Information
------------------

Cristian Marquez Russo.

Based on the work done by Amrit Singh
