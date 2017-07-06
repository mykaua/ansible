# ansible

Installing zabbix-agent on servers using Ansible.
Zabbix-agent can be installed on these OS: Centos 6 and 7, Ubuntu 14.04 and Ubuntu 16.04


We have two main playbooks:

   1) zabbix-agent.yml - playbook for installing zabbix-agent without roles
   2) zabbix-agent-roles.yml - playbook for installing zabbix-agent with roles


What do you need to change? You need to change a few files:
   1) Add Server List(IPs) to "inventory" file
   2) Add the IP of zabbix-server to config file of agent - zabbix_agentd.conf.j2.
 

===============================================================================
How to fix the issue(python issue) with ubuntu 16.XX:
   1) you can run this command:
          $ ansible -m raw -a "apt-get -y install python-simplejson" Ubuntu16

   2) Or you can run the "fix_ubuntu16.yml" playbook.  
   PLEASE NOTE: you inventory file should have group ubuntu16!!!
================================================================================
