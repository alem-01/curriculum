# Network. Connecting Containers.

Until now you started containers separately from one another.

Docker allows you to group containers, so that they can communicate with each other.
For example, _API application_ that need to connect to _database_, that both are running 
in different containers.

## Exercises

1. **Create network**

File: `create_network.sh`

Write script that creates bridge network with name `lrn_network`.
___

2. **Database!**

File: `setup_database.sh`

Write script that runs `postgres:12` in network `lrn_network`. Give container `--name=postgres`

Container should be run with following _env_ variables:
```bash
POSTGRES_PASSWORD=lrn_password
PGDATA=/var/lib/postgresql/data/pgdata
```
___

3. **Fill the database**

File: `fill_database.sh`

In your repo you will find `network/fill.sql`. It contains set of instructions to fill the database.

Write script that does the following:
- executes command in `postgres` container `CREATE DATABASE book_store;`
- executes _sql_ commands in `postgres` container from the `fill.sql` file.

> `exec -i` flag to read from file
___

4. **Launch the app**

File: `Dockerfile, build_app.sh, launch_app.sh`

Dockerize the _Go app_ located in `network/api_application`:
- Create _Dockerfile_

In `build_app.sh` write script that builds image for _Go app_ and tags it `api_application:1.0`.

In `launch_app.sh` write script that runs `api_application:1.0` with following requirements:
- Run in network `lrn_network`
- Set env variables required in `network/api_application/README.MD`
- Set container name `api_application`
- Set port forwarding `8000` to application's inner port
___

5. **Compose**

File: `docker-compose.yml`

Recreate aforementioned exercises by using [docker-compose](https://docs.docker.com/compose/gettingstarted/#step-3-define-services-in-a-compose-file).

Declare services: _postgres_, _api\_application_

Set its container names to _postgres_ and _api\_application_ respectively.

In `api_application/docker-entrypoint-initdb.d` directory there is a script that will be run on database start.
You should copy `network/fill.sql` to `api_application/docker-entrypoint-initdb.d`.
In `init_db.sh` write code that will create the database and fill it using `fill.sql`.

Postgres service:
- image to `postgres:12`
- mount volume `./docker-entrypoint-initdb.d:/docker-entrypoint-initdb.d`

> In api_application service use [build](https://docs.docker.com/compose/compose-file/#build) instead of image

> Set env variables using [environment](https://docs.docker.com/compose/compose-file/#environment)

> No need to create network
