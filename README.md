# Docker-Mini-Project-SYS265
Mini project for SYS-265

> I want to utlize `git` for this assignmnet and this repository will be very important.

Goal: Deploy [Prometheus](https://prometheus.io/docs/introduction/overview/) a system monitoring service via Docker

This service uses the docker-compose sysntax the same type we used to install Wordpress.

Were working with a file system that includes a compose folder for Prometheus and two sub-folders grafana-config & prometheus-config. Each folder will house their respective `.yml` file. Along with this we have one `.yaml` file in the main Prometheus folder. 

The modification occurs in the main `compose.yaml` file. I'm going to change the admin username and password so we dont have to use the default user credentials.



```
 environment:
      - GF_SECURITY_ADMIN_USER=diego
      - GF_SECURITY_ADMIN_PASSWORD=ILOVESYS265
```
