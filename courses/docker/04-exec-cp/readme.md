# To exec, or not to exec

Docker allows you to execute commands inside running container. This can be used to debug, fix bugs etc.
Also, you can send files from local computer to running container or vice versa.

Repository: <a href="https://github.com/alem-classroom/student-docker-${GITHUB_LOGIN}/tree/master/exec-cp" class="repo-button">Exec Cp</a>

## Exercises

1. **Send me to the moon!**

File: `send_backup.sh`

In your repo you will find `exec-cp/postgres.backup`. You will need to restore database backup to `postgres`.

Write script that:
- runs docker container image `postgres:12` with following requirements:
    - detached mode
    - set env variable POSTGRES_PASSWORD=password
    - give it a name `postgres`
- sends `postgres.backup` to root directory of the running container with name `postgres`.
___

2. **Restore backup**

File: `restore_backup.sh`

Write a script that executes following sql scripts in `postgres` container:
- `psql -U postgres -c "CREATE DATABASE exec_cp_database"`
- `psql -U postgres -d exec_cp_database -f /postgres.backup`.
___

3. **Add some songs**

File: `add_songs.sh`

Write script that executes inside `postgres` container `INSERT` queries into database.

You need to add 5 different from existing songs to `songs` table.
```sql
INSERT INTO songs (author, name) VALUES ('Elvis Presley', 'Blue Suede Shoes')
```

> To call sql query in database `psql -U postgres -d <database_name>`
___

4. **Dont forget to backup!**

File: `backup.sh`

Write script that backups `exec_cp_database` and saves to `exec-cp/new_postgres.backup`.

> To back the database: `pg_dump -U postgres exec_cp_database`
