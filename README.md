# 'Бойко Владислав' '**Система мониторинга Zabbix**'
---
# Задание 1
## Команды для установки
1. 'su -'
2. 'apt update'
3. 'apt install postgresql'
4. 'wget https://repo.zabbix.com/zabbix/6.0/debian/pool/main/z/zabbix-release/zabbix-release_6.0-4+debian11_all.deb'
5. 'dpkg -i zabbix-release_6.0-4+debian11_all.deb'
6. 'apt update'
7. 'apt install zabbix-server-pgsql zabbix-frontend-php php7.4-pgsql zabbix-apache-conf zabbix-sql-scripts zabbix-agent'
8. 'sudo -u postgres createuser --pwprompt zabbix'
9. 'sudo -u postgres createdb -O zabbix zabbix'
10. 'zcat /usr/share/zabbix-sql-scripts/postgresql/server.sql.gz | sudo -u zabbix psql zabbix'
11. 'nano /etc/zabbix/zabbix_server.conf - редактируем DBPassword'
12. 'systemctl restart zabbix-server zabbix-agent apache2'
13. 'systemctl enable zabbix-server zabbix-agent apache2'

