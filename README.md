# Docker-Mini-Project-SYS265
Mini project for SYS-265

> I want to utlize `git` for this assignmnet and this repository will be very important.

Goal: Deploy [Prometheus](https://prometheus.io/docs/introduction/overview/) a system monitoring service via Docker

This service uses the docker-compose sysntax the same type we used to install Wordpress.

Were working with a file system that includes a compose folder for Prometheus and two sub-folders grafana-config & prometheus-config. Each folder will house their respective `.yml` file. Along with this we have one `.yaml` file in the main Prometheus folder. 

The modification occurs in the main `docker-compose.yaml` file. I'm going to change the admin username and password so we dont have to use the default user credentials. This cred change is for [Grafana](https://grafana.com/oss/grafana/).


 This is the piece of code we'll be changing.
 
```
 environment:
      - GF_SECURITY_ADMIN_USER=diego
      - GF_SECURITY_ADMIN_PASSWORD=ILOVESYS265!
```

After this has been changed we can start our deployment. For ease of use I'm trying out git.

To install git for Unbuntu use the command `sudo apt install git`. The url of this repo is `https://github.com/dpzrz/Docker-Mini-Project-SYS265.git`.

On our `mgmnt` box were going to PuTTy into our docker box. The ~ directory should have no files and we wont need to create a folder as git will do that for us.

The git command used to copy this repository is `git clone` then after enter the url you see when you click the green code button drop-down menu. After this command you can see the folder from my repo and all the .yml and .yaml files.

<img width="258" alt="image" src="https://github.com/dpzrz/Docker-Mini-Project-SYS265/assets/112894794/96a6d04a-837d-4818-9e77-d83a707cb144">

Just cd into the main folder and use the command `docker-compose up -d` this should start and install the cointaiiners, check the status of the newly installed cointainers using `docker ps`. This command also allowys you to see which ports you'll need to enter for our URL. Navigate to your IP address the add : along with the port number for Prometheus and Graphana.
