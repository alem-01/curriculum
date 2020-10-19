# Hello, Docker!

This is first lesson to get started with docker!

We recommend you to start with [Docker curriculum](https://docker-curriculum.com/).
You will get understanding of how to install Docker and how it works from inside.

In a nutshell, _docker_ is a tool to run applications in isolated environment. This allows to run any application on any server with the same behaviour.

In this lesson you will be introduced to basic docker usage: commands (`run container, list containers, list images and removing both images and containers`), flags and volume mounting.

Have fun!

## Exercises

1. **Run, Docker, Run!**

File: `run_nginx.sh`

To start your first exercise - you need to run your own **WEB SERVER** _nginx_. nginx is an application that serves HTML web-pages, forwards your connection to backend and many many more. But this course is about docker, so we will focus on docker.

Write a bash script to run `nginx:1.19` container on port _80_ and give it a name `nginx-container`.

```bash
docker # ... your commands
```

After running the container, check out your [localhost](http://localhost)

> Run in `detached` mode by default for all exercises

> Read about [port](https://docs.docker.com/config/containers/container-networking/#published-ports)
___

2. **trapped HTML**

File: `mount_dir.sh`

So, you have started nginx server. Mostly, people want to show their own HTML web-site instead of default nginx "Welcome page". So, in this exercise you will learn how to do so.

In your repository you will find `hello/trapped_html` folder with `index.html`. 

Write script that runs `nginx:1.19` container and mounts the `trapped_html` directory  
container, so that it appears on [_home_ page](http://localhost).

You should do following steps:
- detached mode
- port forwarding 80:80
- mount directory
- give container name `nginx-container`

Example:
```bash
docker # ... port to 80 and mount directory
```

After running the container, [localhost](http://localhost) page should be changed.

> To stop previous created container use: `docker stop nginx-container` and then `docker rm nginx-container`

> How to mount directory: [mount volume](https://www.digitalocean.com/community/tutorials/how-to-share-data-between-the-docker-container-and-the-host)

> Mount path should be `/usr/share/nginx/html`
___

3. **Show all containers**

File: `show_containers.sh`

You have run containers, imagine 100! Now you need be able to see all containers, including currently running, exited and those that are trying to restart.

Write script that _shows_ all containers, including _exited_ ones.

> Check out: [ps](https://docs.docker.com/engine/reference/commandline/ps/)
___

4. **Images**

File: `list_images.sh`

The same as you can list containers - docker allows to list all images that are "downloaded" to your machine.

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

Sometimes you will need to remove docker images. It can happen because of many reasons, for example to free up memory space.

Write script that _removes_ `nginx:1.19` image.
