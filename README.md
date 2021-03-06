<p><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Cassandra_logo.svg/1280px-Cassandra_logo.svg.png" alt="cassandra logo" title="cassandra" align="right" height="60" /></p>

# Ansible Role: cassandra

[![Build Status](https://travis-ci.org/paulfantom/ansible-cassandra.svg?branch=master)](https://travis-ci.org/paulfantom/ansible-cassandra)
[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![Ansible Role](https://img.shields.io/badge/ansible%20role-paulfantom.cassandra-blue.svg)](https://galaxy.ansible.com/paulfantom/cassandra/)
[![GitHub tag](https://img.shields.io/github/tag/sointeractive/ansible-cassandra.svg)](https://github.com/paulfantom/ansible-cassandra/tags)

This role installs Cassandra cluster and metrics exporter

## Requirements

Docker must be installed on host system. Due to test requirements those few lines have been commented out from meta/main.yml.

## Example usage

Use it in a playbook as follows:
```yaml
- hosts: cassandra
  become: true
  roles:
    - paulfantom.cassandra
```

Have a look at the [defaults/main.yml](defaults/main.yml) for role variables
that can be overridden.

## Disclaimer

Initial work has been done in [Sointeractive ansible-cassandra](https://github.com/sointeractive/ansible-cassandra) repository.
