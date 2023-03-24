
# CONTAINER


- Vagrant, Docker, Podman let you create portable environments Vagrant helps you set up entire virtual machines to run your applications, Docker/Podman allows you to package an application with its environment and all of its dependencies into a "box", called a container. They both adapted to OCI (Open Container Initiative) standards for images. Usually, a container consists of an application running in a stripped-to-basics version of a Linux operating system. An image is the blueprint for a container, a container is a running instance of an image. Virtual Machine vs Container: VM is complete. Container is closer to the host machine. No emulation of hardware. We share a part of the hardware. disk, network. To do that we segment the harware.

- Docker provides a system-agnostic approach that can create containerized applications across any platform. Podman is a rootless and daemon-less container built explicitly by RedHat to make it better than Docker. Non-root users, too, can use Podman container-based applications.

- Openshift: receives config file and go to pull docker image on nexus to do the deployment. Internal access or external access: Cloudflare can protect external access but not necessary on internal access. There is one BigIP cluster for each access: internal/external, they are responsible to do the load balancing.

- Logging: Fluentd to do the bridge between different log producers. see: kibana, elastic, prometheus (host, memory, cpu, disk), prtg, shinken, pingdom

## ORCHESTRATION

- Container orchestration automates the deployment, management, scaling, and networking of containers. OpenShift, Kubernetes, Apache Mesos or Docker Swarm. OpenShift is considered to be a distribution, that relies on Kubernetes and Helm because Kubernetes is the "kernel" of distributed systems and Helm, the tool for managing package called Charts, indeed a chart is a package of pre-configured Kubernetes resources. it streamlines installing and managing Kubernetes applications. A package contains a Chart.yaml + one or many templates which contain Kubernetes manifest files. Charts can be stored on disk, or fetched from remote chart repositories.

Both Kubernetes and OpenShift are popular container management systems, and each has its unique features and benefits. While Kubernetes helps automate application deployment, scaling, and operations, OpenShift is the container platform that works with Kubernetes to help applications run more efficiently.

OpenShift Online leverages the Kubernetes concept of a pod, which is one or more containers deployed together on one host, and the smallest compute unit that can be defined, deployed, and managed. Pods are the rough equivalent of a machine instance (physical or virtual) to a container.

## LINKS

- https://github.com/containers/podman
- https://github.com/hashicorp/vagrant
- https://github.com/openshift
- https://github.com/docker

## DOCKER

```bash
# container id = cid // image id = iid
docker build . ==> Build the default local Dockerfile
docker build -f Dockerfile.ssr . ==> Build a specific local Dockerfile
docker logs <cid> ==> Displays the container logs
docker run -it $(docker build -q .) ==> Build & Run inline the image in localhost
docker run -p 4200:8080 -d iid ==> Run the image in localhost
docker run -p 4000:4000 -h host.com -d iid ==> Run the image in host.com
docker run -p 4000:4000 -h host.com -v /host/path/to/certs:/container/path/to/certs -d iid "update-ca-certificates" ==> Run the image in host.com with certificate
docker top cid ==> Displays the containers running processes
docker port cid ==> Lists containers port mappings
docker kill cid ==> Kills the process but its not ideal
docker diff cid ==> check changes to files&didirectories
```

## PODMAN

- The most important options when using podman are:
-v (volume) (build|run) which allows to bind volume between the host and the container like this: -v /HOST-DIR:/CONTAINER-DIR. both directories must be absolute. you can use pwd to target the root of the current directory, you can use multiple times the option to mount multiple volumes. ex: -v $(pwd):/opt/apptobuild:U -v $(pwd)/conf:/conf:U
-e (env) (build|run) to pass environment variable to the build or to the process to be run. beware it's quite different behavior between build and run, of course you can use multiple times the option, ex: -e 'spring.profiles.active=dev' -e 'spring.config.location=file:conf/application.properties,file:conf/credential.properties'
-t (tag) (build) simply to define a name to the resulting image if the build process completes successfully. ex: -t appname:type
-f (file) (build) simply to target a custom docker file name different than the classic local Dockerfile. usually it can be to specify a custom local file with an extension type like for the frontend image: Dockerfile.fedev. It can alo be an url with http or https

- https://docs.podman.io/en/latest/markdown/podman-build.1.html
- https://docs.podman.io/en/latest/markdown/podman-run.1.html
- https://docs.podman.io/en/latest/markdown/podman-volume.1.html
- https://www.orpiske.net/2021/10/configuring-intellij-to-work-with-podman/
- https://www.lemagit.fr/conseil/Conteneurisation-les-differences-cles-entre-Docker-et-Podman
- https://www.imaginarycloud.com/blog/podman-vs-docker/
- https://github.com/containers/podman-compose



## VAGRANT

```bash
# ensure that .vagrant/machines/default/virtualbox/creator_uid is 0
sudo vagrant up
sudo vagrant halt
sudo vagrant ssh
sudo yum -y install phpmyadmin
mysql -u root example -- just test
ifconfig (add IP ADRESS 192.168.50.52 + remote DENY )
# KEYS: INSERT +  CTRL C + :w + :q
sudo vim /etc/httpd/conf.d/phpMyAdmin.conf
sudo service httpd restart
```

```bash
vim /etc/phpMyAdmin/config.inc.php

$cfg['Servers'][$i]['AllowNoPassword'] = TRUE;
+ MODIFY USER : root + secret

http://192.168.50.52/phpmyadmin 
root secret
exit
```

## DEBUG

```bash
RUN echo "PWD is: $PWD"
RUN ls
```