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
user$ mkdir docker
user$ cd docker
user$ mkdir containers
user$ sd-container create ubuntu --image=ubuntu:latest
[2017-02-20 00:51:33] [INFO‧‧‧] No local image "ubuntu:latest" found.
[2017-02-20 00:51:35] [INFO‧‧‧] Remote image "ubuntu" found.
[2017-02-20 00:51:37] [INFO‧‧‧] Remote image "ubuntu" and remote "latest" found.
[2017-02-20 00:51:37] [INFO‧‧‧] Container "ubuntu" was successfully created
user$ sd-container status ubuntu
nonexistent
user$ sd-container start ubuntu
[2017-02-20 00:59:38] [INFO‧‧‧] Start docker container "ubuntu".
[2017-02-20 00:59:39] [SUCCESS] Container "ubuntu" was successfully started.
user$ sd-container status ubuntu
running
user$ sd-container login ubuntu
root@54034bd5f559:/# exit
exit
user$ sd-container remove ubuntu
[2017-02-20 01:00:58] [SUCCESS] Docker container "ubuntu" was successfully removed.$
```

```
user$ sd-container stop ixno.apache.php7
[2018-08-13 08:23:00] [SUCCESS] Container "ixno.apache.php7" was successfully stopped.
user$ sd-container remove ixno.apache.php7
[2018-08-13 08:25:43] [SUCCESS] Docker container "ixno.apache.php7" was successfully removed.
user$ sd-image ixno.apache.php7 remove
[2018-08-13 08:26:17] [SUCCESS] Docker image "ixno.apache.php7" was successfully removed.
user$ sd-image ixno.apache.php7 build
user$ sd-container start ixno.apache.php7
[2018-08-13 08:30:10] [INFO‧‧‧] Start docker container "ixno.apache.php7".
[2018-08-13 08:30:11] [INFO‧‧‧] activate http ..
[2018-08-13 08:30:11] [INFO‧‧‧] done
[2018-08-13 08:30:11] [INFO‧‧‧] start apache ..
[2018-08-13 08:30:12] [INFO‧‧‧] done
[2018-08-13 08:30:12] [INFO‧‧‧] start postfix ..
[2018-08-13 08:30:13] [INFO‧‧‧] done
[2018-08-13 08:30:13] [SUCCESS] Container "ixno.apache.php7" was successfully started.
```

## A. Authors

* Björn Hempel <bjoern@hempel.li> - _Initial work_ - [https://github.com/bjoern-hempel](https://github.com/bjoern-hempel)

## B. Licence

This tutorial is licensed under the MIT License - see the [LICENSE.md](/LICENSE.md) file for details

## C. Closing words

Have fun! :)
