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

![img](https://github.com/VladiSlave2042/-Zabbix/blob/main/img/1.1.png)
---

# Задание 2

## Команды для установки
1. 'su -'
2. 'apt update'
3. 'wget https://repo.zabbix.com/zabbix/6.0/debian/pool/main/z/zabbix-release/zabbix-release_6.0-4+debian11_all.deb'
4. 'dpkg -i zabbix-release_6.0-4+debian11_all.deb'
5. 'apt update'
6. 'apt install zabbix-agent'
7. 'systemctl restart zabbix-agent'
8. 'systemctl enable zabbix-agent'
9. 'nano /etc/zabbix/zabbix_agentd.conf' - добавляем ip сервера

![latest_data](https://github.com/VladiSlave2042/-Zabbix/blob/main/img/latest_data.png)

![tail_log](https://github.com/VladiSlave2042/-Zabbix/blob/main/img/tail_log.png)

![host_conect](https://github.com/VladiSlave2042/-Zabbix/blob/main/img/%D0%BF%D0%BE%D0%B4%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D1%8B.png)