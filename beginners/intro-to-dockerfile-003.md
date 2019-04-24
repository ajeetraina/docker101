# What is Dockerfile

The humble but powerful Dockerfile is the building block of Docker images and containers. In essence, it's a list of commands the Docker engine runs to assemble the image, and thus instances of images as containers.

## Building Nginx Docker Image using Dockerfile

```bash
git clone https://github.com/ajeetraina/docker101
cd docker101/beginners/nginx
```

```bash
docker build -t ajeetraina/mynginx .
```

```bash
docker inspect <containerid>
```

```bash
[node2] (local) root@192.168.0.7 ~
$ docker inspect 8f| grep Vendor
                "Vendor": "Collabnix Products",
                "Vendor": "Collabnix Products",
[node2] (local) root@192.168.0.7 ~
$
```

## What if I have multiple Dockerfiles under the same directory

```bash
docker build -t ajeetraina/mynginx -f ./nginx1.Dockerfile .
```

## Demonstrating CMD

Create a file called cmd.Dockerfile and add the below content:

```bash
FROM ubuntu
CMD echo "This is a test." | wc -
```

Now build Docker Image

```bash
docker build -t ajeetraina/mycmd -f ./cmd.Dockerfile .
```

Now if you run it:

```bash
docker run ajeetraina/mycmd
```

```bash
$ docker run ajeetraina/wc
      1       4      16 -
```

## Dockerfile: CMD

### Example:1

```bash
FROM ubuntu:14.04
CMD ["/bin/echo" , "Hi Docker !"]
```

```bash
...
$ docker run eff764828551
Hi Docker !
```

[[Next: Hello World 001]](https://github.com/ajeetraina/docker101/blob/master/beginners/hello-world-001.md)
