How to run the Dairy Farm Shop Management System Project (DFSMS)
=================================================================
1. Download the zip file

2. Extract the file and copy dfsms folder

3.Paste inside root directory(for xampp xampp/htdocs, for wamp wamp/www, for lamp var/www/html)

4. Open PHPMyAdmin (http://localhost/phpmyadmin)

5. Create a database with name dfsms

6. Import dfsms.sql file(given inside the zip package in SQL file folder)

7.Run the script http://localhost/dfsms


==================================================================
STEPS to run the Dairy Farm Shop Management System Project (DFSMS)
===================================================================
APPLICATION SERVER:-
-------------------
1. deploy the application[dfsms] in the respective path given below,
      /var/www/html/

2. add the db.php file in this place[/var/www/html/] and run this to check the connection.
      >> Here we are using mysql server. So, we need just for the server which is related/supports to the mysqli code 
      >> If we are using the deferent server instead of mysql server then we need to use respective code which is support to that server.
      >> Then add the database detailes here, save and run the following file to check the connection.

3. change the confiiguration of the sql in the application server in both " db.php " and also " /var/www/html/includes/config.php "


DATABASE SERVER :-
-----------------

1. Install the latest/specific MYSQL server make sure this is running as expected.
      sudo apt update
      sudo apt upgrade
      sudo apt install mysql-server
      mysqld --version

2. Securing MySQL.
      sudo mysql_secure_installation

3. Check the status of the mysql server we insatlled, it should be active.
      sudo systemctl status mysql

4. Log in to MySQL Server.
      sudo mysql -u root

      >> show databases;
      >> create database <db_name>;
      >> show databases;
      >> use <db_name>;
      >> exit

5. Give the remote access permision to the database server.
[ change the bind adress here in the mentioned path to 0.0.0.0 ]
      sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf

6. Add  the database file to the created database.
      mysql -u <user_name> -p <db_name> < dfsms.sql 

7. After the following process we need to do the configuration for the database server, create new user and password, use give the previlages for the database we created etc.






