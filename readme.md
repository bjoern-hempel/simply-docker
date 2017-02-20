# simply-docker

> Simply manage your docker images and containers.


## Install

```
$ mkdir simply-docker
$ cd simply-docker
$ git clone git@github.com:bjoern-hempel/simply-docker.git .
$ sudo ./install
[2017-02-20 00:41:09] [INFO‧‧‧] ┏━  Try to install the given script
                                ┃   /home/user/simply-docker/bin/image to
                                ┗━  /usr/local/bin/sd-image.
[2017-02-20 00:41:09] [SUCCESS] ┏━  The given script
                                ┃   /home/user/simply-docker/bin/image
                                ┗━  was successfully installed to 
[2017-02-20 00:41:09] [INFO‧‧‧] ┏━  Try to install the given script
                                ┃   /home/user/simply-docker/bin/container to
                                ┗━  /usr/local/bin/sd-container.
[2017-02-20 00:41:09] [SUCCESS] ┏━  The given script
                                ┃   /home/user/simply-docker/bin/container
                                ┗━  was successfully installed to
```


## Usage

```
$ mkdir docker
$ cd docker
$ mkdir containers
$ sd-container create ubuntu --image=ubuntu:latest
[2017-02-20 00:51:33] [INFO‧‧‧] No local image "ubuntu:latest" found.
[2017-02-20 00:51:35] [INFO‧‧‧] Remote image "ubuntu" found.
[2017-02-20 00:51:37] [INFO‧‧‧] Remote image "ubuntu" and remote "latest" found.
[2017-02-20 00:51:37] [INFO‧‧‧] Container "ubuntu" was successfully created
$ sd-container status ubuntu
nonexistent
$ sd-container start ubuntu
[2017-02-20 00:59:38] [INFO‧‧‧] Start docker container "ubuntu".
[2017-02-20 00:59:39] [SUCCESS] Container "ubuntu" was successfully started.
$ sd-container status ubuntu
running
$ sd-container login ubuntu
root@54034bd5f559:/# exit
exit
$ sd-container remove ubuntu
[2017-02-20 01:00:58] [SUCCESS] Docker container "ubuntu" was successfully removed.$
```

## License

ISC © [Björn Hempel](https://www.ixno.de)
# 
