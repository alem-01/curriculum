# Hello, Docker!

This is first lesson to get started with docker!

We recommend you to start with [Docker curriculum](https://docker-curriculum.com/).
You will get understanding of how to install Docker and how it works from inside.


## Exercises

1. **Run, Docker, Run!**

File: `run_nginx.sh`

Write a bash script to run `nginx` container on port _80_ and give it a name `nginx-container`.

```bash
docker # ... your commands
```

> run in `detached` mode by default for all exercises
> [port](https://docs.docker.com/config/containers/container-networking/#published-ports)
___

2. **trapped HTML**

File: `mount_dir.sh`

In your template you will find `hello/trapped_html` folder with `index.html`. 

Write script that runs `nginx` container and mounts the `trapped_html` directory  
container, so that it appears on _home_ page `localhost:80/`.
- port forwarding 80:80
- mount directory
- give container name `nginx`

```bash
docker # ... port to 80 and mount directory
```

> [mount volume](https://www.digitalocean.com/community/tutorials/how-to-share-data-between-the-docker-container-and-the-host)

> mount to directory `/usr/share/nginx/html`
___

3. **Don't stop me now!**

File: `stop_nginx.sh`

Write script that _stops_ container named `nginx`.
___

4. **Show all containers**

File: `show_containers.sh`

Write script that _shows_ all containers, including _exited_ ones.

> [ps](https://docs.docker.com/engine/reference/commandline/ps/)
___

5. **Terminator**

File: `remove_nginx.sh`

Write script that _removes_ container named `nginx`.
___

6. **Images**

File: `list_images.sh`

Write script that _lists_ all images.
___

7. **Bye, nginx!**

File: `rmi_nginx.sh`

Write script that _removes_ `nginx` image.
