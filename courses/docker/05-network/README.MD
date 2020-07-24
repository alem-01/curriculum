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

Write script that runs `postgres:12`:
- detached mode
- in network `lrn_network`.
- env variable `POSTGRES_PASSWORD=lrn_password`
- env variable `PGDATA=/var/lib/postgresql/data/pgdata`
- name `postgres`
___

3. **Fill the database**

File: `fill_database.sh`

In your repo you will find `network/fill.sql`. It contains set of instructions to fill the database.

Write script that does the following:
- executes command in `postgres` container `psql -U postgres -c "CREATE DATABASE book_store;"`
- executes _sql_ commands in `postgres` container from the `fill.sql` file: `psql -U postgres -d book_store`.

> `exec -i` flag to read from file
___

4. **Launch the app**

File: `Dockerfile, build_app.sh, launch_app.sh`

Dockerize the _Go app_ located in `network/api_application`:
- Create _Dockerfile_

In `build_app.sh` write script that builds image for _Go app_ in current directory and tags it `api_application:1.0`.

In `launch_app.sh` write script that runs `api_application:1.0` with following requirements:
- detached mode
- Run in network `lrn_network`
- Set env variables required in `network/api_application/README.MD`
- Set container name `api_application`
- Set port forwarding `8000` to application's inner port

> DB_USER by default is `postgres`

> DB_PASSWORD is specified above

> DB_HOST will become the name of postgres container - `postgres`

> postgres default port is 5432

> DB_DATABASE is specified above too, find it
___

5. **Compose**

File: `docker-compose.yml`

Recreate aforementioned exercises by using [docker-compose](https://docs.docker.com/compose/gettingstarted/#step-3-define-services-in-a-compose-file).

docker-compose allows you to group multiple containers by specifing them in `docker-compose.yml`. Instead of writing long scripts of `docker run ...` docker-compose allows you to describe container characteristics: network, volume, env variables and many many more.

Before doing this exercise get to know this technology.

Use in _docker-compose.yml_ `version: '3'`

Declare services: _postgres_, _api\_application_

_postgres_:
- image: "postgres:12"
- container name: "postgres"
- add environment: `POSTGRES_PASSWORD=lrn_password`
- add environment: `PGDATA=/var/lib/postgresql/data/pgdata`
- mount volume `./docker-entrypoint-initdb.d:/docker-entrypoint-initdb.d`

_api\_application_:
- depends on: "postgres"
- build: "."
- container name: "api\_application"
- add environment required
- port forwarding: 8000 to application's port

In `api_application/docker-entrypoint-initdb.d` directory there is a script that will be run on database start.

You should copy `network/fill.sql` to `api_application/docker-entrypoint-initdb.d`.

In `docker-entrypoint-initdb.d/init_db.sh` write code that will:
- execute `CREATE DATABASE book_store`
- fill `book_store` database using `fill.sql`. (due executing in container you need to specify full path `/docker-entrypoint-initdb.d/fill.sql`)

> In api_application service use [build](https://docs.docker.com/compose/compose-file/#build) instead of image

> Set env variables using [environment](https://docs.docker.com/compose/compose-file/#environment)

> No need to create network
