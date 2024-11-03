# Guide to Installing WordPress on Ubuntu

- Parameters: 	4 vCPU, 8 GB RAM, 90 GB Disk
- ОS: 			    Ubuntu 22.04

## PHP

```bash
sudo apt update
```

```bash
sudo apt install php libapache2-mod-php php-mysql
```

Select options ...
```bash
Restarting services...
Daemons using outdated libraries
--------------------------------

  1. dbus.service                 5. ssh.service               9. systemd-timesyncd.service
  2. getty@tty1.service           6. systemd-journald.service  10. systemd-udevd.service
  3. multipathd.service           7. systemd-logind.service    11. unattended-upgrades.service
  4. networkd-dispatcher.service  8. systemd-resolved.service  12. none of the above

(Enter the items or ranges you want to select, separated by spaces.)

Which services should be restarted?
```

Checking installation
```bash
php -v
```

Restart Apache(if using Apache)
```bash
sudo systemctl restart apache2
```

Install additional PHP modules you may need
```bash
sudo apt install php-curl php-json php-cgi php-gd php-mbstring php-xml php-zip
```

## MySQL

```bash
sudo apt install mysql-server
```

After installation, it’s recommended to run a security script that comes with MySQL to improve its security
```bash
sudo mysql_secure_installation
```

Check MySQL Service
```bash
sudo systemctl status mysql
```

Start MySQL Service
```bash
sudo systemctl start mysql
```

Enable MySQL to Start on Boot
```bash
sudo systemctl enable mysql
```

Log in to MySQL
```bash
sudo mysql -u root -p
```
