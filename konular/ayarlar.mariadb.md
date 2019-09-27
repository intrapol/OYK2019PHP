# MariaDB İçin Parola Belirleme / Sıfırlama

## Güvenli Kurulum Sihirbazı

```BASH
sudo mysql_secure_installation
```
### Yukarıdaki Komutun Çıktı Ekranları ve Cevap Yönergeleri

NOTE: RUNNING ALL PARTS OF THIS SCRIPT IS RECOMMENDED FOR ALL MariaDB
      SERVERS IN PRODUCTION USE!  PLEASE READ EACH STEP CAREFULLY!

In order to log into MariaDB to secure it, we'll need the current
password for the root user.  If you've just installed MariaDB, and
you haven't set the root password yet, the password will be blank,
so you should just press enter here.

Enter current password for root (enter for none): **ENTER BASINIZ**

OK, successfully used password, moving on...

Setting the root password ensures that nobody can log into the MariaDB
root user without the proper authorisation.

Set root password? [Y/n] **ENTER BASINIZ**

New password: **YENİ PAROLA GİRİNİZ**

Re-enter new password: **YENİ PAROLA GİRİNİZ**

Password updated successfully!
Reloading privilege tables..
 ... Success!


By default, a MariaDB installation has an anonymous user, allowing anyone
to log into MariaDB without having to have a user account created for
them.  This is intended only for testing, and to make the installation
go a bit smoother.  You should remove them before moving into a
production environment.

Remove anonymous users? [Y/n] **ENTER BASINIZ**

 ... Success!

Normally, root should only be allowed to connect from 'localhost'.  This
ensures that someone cannot guess at the root password from the network.

Disallow root login remotely? [Y/n] **ENTER BASINIZ**

... Success!

By default, MariaDB comes with a database named 'test' that anyone can
access.  This is also intended only for testing, and should be removed
before moving into a production environment.

Remove test database and access to it? [Y/n] **ENTER BASINIZ**

 - Dropping test database...
 ... Success!
 - Removing privileges on test database...
 ... Success!

Reloading the privilege tables will ensure that all changes made so far
will take effect immediately.

Reload privilege tables now? [Y/n] **ENTER BASINIZ**

 ... Success!

Cleaning up...

All done!  If you've completed all of the above steps, your MariaDB
installation should now be secure.

Thanks for using MariaDB!



## Access denied for user 'root'@'localhost' Uyarısını Kaldırmak

```SQL
sudo mysql -u root
  show databases;
  use mysql;
  update user set plugin='' where User='root';
  flush privileges;
  exit;
```


# Unutulan MySQL Root Parolasının Sıfırlanması
```
sudo service mysql  stop
sudo service mysqld stop
sudo mysqld_safe --skip-grant-tables --skip-networking &
mysql -u root
  use mysql;
  update user set password=PASSWORD("root") where User='root';
  flush privileges;
  quit;
sudo kill `sudo cat /var/run/mysqld/mysqld.pid`
sudo service mysql  start
sudo service mysqld start
```


# Unutulan MariaDB Root Parolasının Sıfırlanması
```
sudo service mariadb  stop
sudo mysqld_safe --skip-grant-tables --skip-networking --skip-networking &
mysql -u root
  use mysql;
  update user set password=PASSWORD("root") where User='root';
  flush privileges;
  quit;
sudo kill `sudo cat /var/run/mysqld/mysqld.pid`
sudo service mariadb start
```

Parola sıfırlaması için [detaylı bilgi burada.](https://www.cloudeos.com/topluluk/mysql-veya-mariadb-root-sifresinin-sifirlanmasi)

