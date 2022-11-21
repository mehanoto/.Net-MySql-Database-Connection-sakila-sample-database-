# Schema
![alt tag](https://raw.githubusercontent.com/Obrelix/.Net-MySql-Database-Connection-sakila-sample-database-/master/Schema/saqila.PNG)

# Инсталация в MySQL 

Ще инсталираме sakila базата в нашия локален Mysql server. Стъпки:
- Отваряме Command prompt 
- Навигираме до %*MY_SQL_INSTALLATION_DIR*%/bin .%*MY_SQL_INSTALLATION_DIR*% e инсталационната папка на MySQL сървъра.
- Въвеждаме и изпълняваме командата по-долу, съответно с нашите user/pass
```
mysql --user=root --password=root
```
- След това създаваме sakila базата
```
> create database sakila;
```
- Излизаме оттук с командата Cntrl + C
- Отново се логваме, само че този път в новосъздадената sakila
```
mysql --user=root --password=root sakila
```
- Изпълняваме скрипта sakila-schema.sql, който създава схемата + някои допълнителни неща за sakila. Тук е важно да заменим %*PROJ_DIR*% с реалното място на проекта, който сме свалили от github.com
```
> source D:\%PROJ_DIR%\.Net-MySql-Database-Connection-sakila-sample-database-\sql\sakila-schema.sql
```
- Изпълняваме и скрипта, който "пълни" базата с данни
```
> source D:\%PROJ_DIR%\.Net-MySql-Database-Connection-sakila-sample-database-\sql\sakila-data.sql
```