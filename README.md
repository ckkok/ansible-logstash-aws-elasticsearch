# Ansible Tasks for Logstash Installation on CentOS and Configuration for AWS Elasticsearch

- Primarily used for AWS EC2 to install Logstash and its AWS Elasticsearch plugin
- Configures Logstash to read an application log file and push it to Elasticsearch directly
- Installs the Logstash system service by invoking `system-install` from the Logstash directory
- Starts the Logstash system service

## Requirements

- Java >= 8 must be installed
- The environment variable `JAVA_HOME` must be set and valid

## Instructions

- Specify the host(s), the ansible user and key files to use in `inventory.yml`
- Configure the AWS region, Elasticsearch endpoint, and application log path in `roles/install-logstash/defaults/main.yml`
- Run `ansible-playbook -i inventory.yml playbook.yml`
