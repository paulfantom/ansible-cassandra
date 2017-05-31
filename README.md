Ansible role to install and configure Cassandra cluster
=======================================
This role installs Cassandra cluster and metrics exporter if required

Role Variables
--------------

Below are the roles variables with the respective default values. Usually you'd only change the cassandra_jmx_exporter_version.
Also pay attention to cassandra_hosts_group varible.
```yml
cassandra_package:
cassandra_hosts_group: "cassandra"

cassandra_cluster_username:
cassandra_cluster_password: 
cassandra_port: 9042
cassandra_interface: "{{ ansible_default_ipv4.interface }}"
#cassandra_address: # Will be set automatically
cassandra_seeds: []

# enable monitoring
cassandra_metrics: true
cassandra_jmx_exporter_version: 0.9
cassandra_jmx_exporter_port: 7080
cassandra_jmx_exporter_url: "https://repo1.maven.org/maven2/io/prometheus/jmx/jmx_prometheus_javaagent/{{ cassandra_jmx_exporter_version }}/jmx_prometheus_javaagent-{{ cassandra_jmx_exporter_version }}.jar"

cassandra_cluster_name: "Test Cluster"

cassandra_num_tokens: 256

cassandra_root_dir: /etc/cassandra
cassandra_data_dirs: 
  - "/var/lib/cassandra/data"
  
cassandra_commitlog_dir: "/var/lib/cassandra/commitlog"
cassandra_saved_caches_dir: "/var/lib/cassandra/saved_caches"
```

Example Playbook
----------------

    - hosts: cassandra
      roles:
         - java
         - cassandra

