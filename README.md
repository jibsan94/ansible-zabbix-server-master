## Ansible Zabbix Server Master

This Role installs Zabbix Server Network Monitoring System. To acces to the Login page you should tipe on a browser:

    http://host_ip/zabbix

The default credentials to login on the System are:

    User: Admin
    Password: zabbix

# Requirements

The Host must have installed `apache2` but it is optional.

# Role Variables

To make changes to the Zabbix Server go to:

    defaults/main.yml

To change the address of the repository change the following line:

    zabbix_ip_repo: 192.168.14.100:8082

Name of the Database on MySQL that Zabbix will be using:

    zabbix_mysql_db_name: zabbix

User and Password of the User to create for Zabbix on MySQL

    zabbix_mysql_user_name: zabbix
    zabbix_mysql_user_password: password

Available variables are listed below for zabbix_server.conf file, along with the default values:

    zabbix_server_db_host: localhost
    zabbix_server_db_name: zabbix
    zabbix_server_db_user: zabbix
    zabbix_server_db_password: password

# Dependencies

    - jibsan94.ansible-mysqldb

# Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: webservers
      roles:
         - { role: jibsan94.ansible-zabbix-server-master }

# License

BSD

## Author Information

# This Role was created by [Eng. Jibsan Joel Rosa Toirac](https://www.facebook.com/jibsanjoel.rosatoirac).
