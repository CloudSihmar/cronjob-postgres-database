# cronjob-postgres-database

Step1 : Apply secret, pv1, pv2, pvc1 and pvc2 yaml files

Step 2: Apply main-postgress and backup-posgres yaml files

Step 3: apply the service file to expose the above deployment

Step 4: Apply cron file to backup the data from backup-postgres and store it in the main-postgres application.
