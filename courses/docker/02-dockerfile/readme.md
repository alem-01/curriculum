# Oh my, Dockerfile

Dockerfile is the file to build images. It has lines of instructions to build the image like: 
- installing dependencies
- setting environmental variables
- exposing ports
- setting entrypoint (commands that run on container start)
- many more...

## Exercises

1. **Python Project**

File: `dockerfile/python-project/Dockerfile`

In your repo you will find `dockerfile/python-project`. It has `README.MD` with instructions on 
how to install dependencies and run the http server.

You will need to create `dockerfile/python-project/Dockerfile` that dockerizes the `python-project`.

Dockerfile must have following:
- set workdir to `/app`
- install dependencies
- set env variable `PORT=3000`
- set env variable `APP_TYPE=Python`
- entry point that runs the application

Create following scripts in root directory:
- `script-build.sh` - builds docker image with tag `python-project:1.0` in current directory.
- `script-run.sh` - runs the project in `detached mode`, port forwarding from 7000 to application's port and gives container name `python-project`.

> [python docker image](https://hub.docker.com/_/python)

> if `Unable to find image 'python-project:latest' locally` then specify the image tag

> if `Error: Invalid value for '--port': $PORT is not a valid integer` then PORT variable is passed incorrectly. Figure out how to do it.
___

2. **Node Project**

File: `dockerfile/node-project/Dockerfile`

In your repo you will find `dockerfile/node-project`. It has `README.MD` with instructions on 
how to install dependencies and run the http server.

You will need to create `dockerfile/node-project/Dockerfile` that dockerizes the `node-project`.

Dockerfile must have following:
- set workdir to `/app`
- install dependencies
- entry point that runs the application

Create following scripts in root directory:
- `script-build.sh` - builds docker image with tag `node-project:1.0` in current directory.
- `script-run.sh` - runs the project in `detached mode` with env variables `PORT=4000`, `APP_TYPE=Node`, port forwarding from 8000 to application's port and gives container name `node-project`.
___

3. **Go Project**

File: `dockerfile/go-project/Dockerfile`

In your repo you will find `dockerfile/go-project`. It has `README.MD` with instructions on 
how to install dependencies and run the http server.

You will need to create `dockerfile/go-project/Dockerfile` that dockerizes the `go-project`.

Dockerfile must have following:
- set workdir to `/go/src/go-project`
- install dependencies
- entry point that runs the application

Create file `.env` in project directory which will store env variables:
```bash
PORT=5000
APP_TYPE=Go
```

Create following scripts in root directory:
- `script-build.sh` - builds docker image with tag `go-project:1.0` in current directory.
- `script-run.sh` - runs the project in `detached mode` with including of env variables from file `.env`, port forwarding from 9000 to application's port and name given `go-project`.
