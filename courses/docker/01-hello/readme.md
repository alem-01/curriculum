# Hello, Docker!

This is first lesson to get started with docker!

We recommend you to start with [Docker curriculum](https://docker-curriculum.com/).
You will get understanding of how to install Docker and how it works from inside.

## Exercises

1. **Run, Docker, Run!**

File: `run_nginx.sh`

Write a bash script to run `nginx:1.19` container on port _80_ and give it a name `nginx-container`.

```bash
docker # ... your commands
```

After running the container, check out your [localhost](http://localhost)

> run in `detached` mode by default for all exercises

> [port](https://docs.docker.com/config/containers/container-networking/#published-ports)
___

2. **trapped HTML**

File: `mount_dir.sh`

In your template you will find `hello/trapped_html` folder with `index.html`. 

Write script that runs `nginx:1.19` container and mounts the `trapped_html` directory  
container, so that it appears on _home_ page `localhost:80/`.
- port forwarding 80:80
- mount directory
- give container name `nginx`

```bash
docker # ... port to 80 and mount directory
```

After running the container, [localhost](http://localhost) page should be changed.

> to stop previous created container use: `docker stop nginx-container` and then `docker rm nginx-container`

> [mount volume](https://www.digitalocean.com/community/tutorials/how-to-share-data-between-the-docker-container-and-the-host)

> mount to directory `/usr/share/nginx/html`
___

3. **Show all containers**

File: `show_containers.sh`

Write script that _shows_ all containers, including _exited_ ones.

> [ps](https://docs.docker.com/engine/reference/commandline/ps/)
___

4. **Images**

File: `list_images.sh`

Write script that _lists_ all images in format `{{.Size}}\t{{.Repository}}:{{.Tag}}\t{{.ID}}` and sorts by size descending.

```bash
88,1MB  node:lts-alpine                             927d03058714
72,9MB  ubuntu:eoan                                 2f6c85efea61
64,2MB  ubuntu:18,04                                2eb2d388e1a2
```

> Replace dots `.` in size to comma `,`.

> Use `column -t` to format pretty as above example
___

5. **Bye, nginx!**

File: `rmi_nginx.sh`

Write script that _removes_ `nginx:1.19` image.
