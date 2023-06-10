# cronjob-postgres-database

Step1 : Apply secret, pv1, pv2, pvc1 and pvc2 yaml files

Step 2: Apply main-postgress and backup-posgres yaml files

Step 3: apply the service file to expose the above deployment

Step 4 : access the backup database and create a table with some content.

kubectl exec -it backup-postgres -- /bin/bash

sql -U admin -d postgres

CREATE TABLE employees1 ( id SERIAL PRIMARY KEY, name VARCHAR ( 100 ), age INTEGER, department VARCHAR (100));

INSERT INTO employees1 (name, age, department) VALUES ( 'Sandeep', 30, 'IT'),('Sam', 35, 'HR'),('Kavi', 35, 'Accounts'),('Aamir', 30, 'Devops');

# check the tables
/dt   
select * from employees;

Step 5: Apply cron file to backup the data from backup-postgres and store it in the main-postgres application.

Step 6 : now check the main-postgres database if the data has been uploaded or not.


