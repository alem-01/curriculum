# To exec, or not to exec

Docker allows you to execute commands inside running container. This can be used to debug, fix bugs etc.
Also, you can send files from local computer to running container or vice versa.

## Exercises

1. **Send me to the moon!**

File: `send_backup.sh`

In your repo you will find `exec-cp/postgres.backup`. You will need to restore database backup to running inside 
container `postgres`. You will need to send backup file to running `postgres` container.

Run docker container image `postgres:12`.

Write script that sends `postgres.backup` to root directory of the running container with name `postgres`.
___

2. **Restore backup**

File: `restore_backup.sh`

Write a script that restores backup file to database in `postgres` container.

> Before restoring from backup you need to create database with name _exec\_cp\_database_ and restore to it the backup

3. **Add some songs**

File: `add_songs.sh`

Write script that executes inside container `INSERT` queries into database.

You need to add 5 different from existing songs to `songs` table.

4. **Dont forget to backup!**

File: `backup.sh`

Write script that backups `exec_cp_database` and saves to `exec-cp/new_postgres.backup`.

> Use exec and cp
