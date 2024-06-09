# :memo: Notes
## MYSQL
---
### Resources
- [MySQL](https://www.mysql.com/)
- [Workbench](https://www.mysql.com/products/workbench/)
#### Help
- [How to Install MySQL WorkBench on Ubuntu?](https://www.geeksforgeeks.org/how-to-install-mysql-workbench-on-ubuntu/)
- [How To Install MySQL on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04)
### Terms and concepts
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
#### Basic setup
Installing MySQL
```
$ apt-get update
$ apt install mysql-server
$ systemctl is-active mysql
$ systemctl status mysql.service
$ systemctl start mysql.service
$ systemctl stop mysql.service
$ systemctl restart mysql.service
$ mysql
mysql> \q or exit
```
Configure MySQL server
```
$ mysql_secure_installation

$ mysql
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
mysql> exit or \q
```
Workbench Installation
```
$ snap install mysql-workbench-community
```
---
## Software Developer
Built by [javi](https://github.com/javierandres-dev/) :copyright: 2024  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javierandres-dev/).
