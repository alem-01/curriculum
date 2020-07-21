# Hello, Docker!

This is first lesson to get started with docker!

We recommend you to start with [Docker curriculum](https://docker-curriculum.com/).
You will get understanding of how to install Docker and how it works from inside.


## Exercises

1. **Run, Docker, Run!**

Write a bash script to run `nginx` container on port _80_ and give it a name `nginx-container`.

```bash
docker # ... your commands
```

> run in `detached` mode by default for all exercises
> [port](https://docs.docker.com/config/containers/container-networking/#published-ports)

2. **trapped HTML**

In your template you will find `trapped_html` folder with `index.html`. 
Write script that mounts the `trapped_html` directory to `nginx` docker 
container, so that it appears on _home_ page `localhost:80/`.

```bash
docker # ... port to 80 and mount directory
```

> [mount volume](https://www.digitalocean.com/community/tutorials/how-to-share-data-between-the-docker-container-and-the-host)

3. **Don't stop me now!**

Write script that _stops_ your running `nginx`.

4. **Show all containers**

Write script that _shows_ all containers, including _exited_ ones.

> [ps](https://docs.docker.com/engine/reference/commandline/ps/)

5. **Terminator**

Write script that _removes_ `nginx` container.