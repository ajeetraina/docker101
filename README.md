# Docker for You (DFY)

** THIS IS AN OLD REPOSITORY. Please refer [DockerLabs](http://dockerlabs.collabnix.com) if you want to get started with Docker] **

Are you new to Docker? Want to build your career in Container Technology?

Then Welcome ! You are at the right place.

This repository brings you tutorials that help you get hands-on experience using Docker. Here you will find a mix of labs and tutorials that will help you, no matter if you are a beginner, SysAdmin, IT Pro or Developer. Yes, you read it correct ! Its $0 learning platform. You don't need any infrastructure. Most of the tutorials runs on [Play with Docker Platform](http://play-with-docker.com). This is a free browser based learning platform for you. Docker tools like Docker Engine, Docker Compose & Docker Machine are already installed for you. All you need is to get started.

## Getting Started with Docker

To get started with Docker, follow the below steps:

- Create Dockerhub Account
- Open [Play with Docker Platform](http://play-with-docker.com)
- Click on "Start"
- This will open up an easy to understand PWD(Play with Docker) tool which displays instances on the left hand side while terminal at the right hand side
- Click on "Create Instance" to create your first Linux instance

## Getting Started with Docker Swarm

To get started with Docker Swarm, you can use "Play with Docker", shortly called PWD. It's free of cost and open for all.
You get maximum of 5 instances of Linux system to play around with Docker.

- Open [Play with Docker Labs](https://labs.play-with-docker.com) on your browser
- Click on the icon near to Instance to choose 3 Managers & 2 Worker Nodes

![My image](https://github.com/ajeetraina/docker101/blob/master/images/pwd_1.png)

- Wait for few seconds to bring up 5-Node Swarm Cluster

We recommend you start with one of our Beginners Guides, and then move to intermediate and expert level tutorials that cover most of the features of Docker. For a comprehensive approach to understanding Docker, I have categorized it as shown below:

[Docker for Beginners](https://github.com/ajeetraina/docker101/tree/master/beginners/README.md)

[Docker for Intermediate](https://github.com/ajeetraina/docker101/tree/master/intermediate/README.md)

[Docker for Advanced Users](https://github.com/ajeetraina/docker101/tree/master/advanced/README.md)

## A Bonus... Docker Swarm Visualizer

Swarm Visualizer is a fancy tool which visualized the Swarm Cluster setup. It displays containers running on each node in the form of visuals. If you are conducting Docker workshop, it's a perfect way to show your audience how the containers are placed under each node. Go..try it out..

## Clone the Repository

```bash
git clone https://github.com/dockersamples/docker-swarm-visualizer
```

```bash
cd docker-swarm-visualizer
docker-compose up -d
```

![My image](https://github.com/ajeetraina/docker101/blob/master/images/visualizer.png)

To run in a docker swarm:

```bash
$ docker service create \
  --name=viz \
  --publish=8080:8080/tcp \
  --constraint=node.role==manager \
  --mount=type=bind,src=/var/run/docker.sock,dst=/var/run/docker.sock \
  dockersamples/visualizer
```

## Docker-Ready Solution for You

[WordPress under Docker Swarm](https://github.com/ajeetraina/docker101/tree/master/play-with-docker/wordpress/example1/README.md)

[ELK under Docker Swarm](https://github.com/ajeetraina/docker101/tree/master/play-with-docker/ELK/README.md)

[Prometheus Stack under Docker Swarm](https://github.com/ajeetraina/docker101/tree/master/play-with-docker/docker-prometheus-swarm/README.md)

[Apache Jmeter under Docker Swarm Mode](https://github.com/ajeetraina/docker101/tree/master/play-with-docker/jmeter-docker/README.md)

[Voting App Example](https://github.com/ajeetraina/docker101/tree/master/play-with-docker/example-voting-app/README.md)

[Playing around with Photon OS](https://github.com/ajeetraina/docker101/tree/master/play-with-docker/vmware/powercli/README.md)

[Playing around with MacVLAN](https://github.com/ajeetraina/docker101/tree/master/play-with-docker/macvlan/README.md)

[IPv6 & Docker Compose](https://github.com/ajeetraina/docker101/tree/master/play-with-docker/ipv6/README.md)

[Trying out Gitlab](https://github.com/ajeetraina/docker101/tree/master/play-with-docker/gitlab/README.md)

[Getting Started with Nginx](https://github.com/ajeetraina/docker101/tree/master/play-with-docker/nginx/README.md)
