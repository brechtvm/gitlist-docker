gitlist-docker
==============

A ready to use docker image with preinstalled nginx and gitlist.

You can use it to quickly expose a web interface of the git repositories in a
directory of your host machine.

The dockerfile uses the lastest gitlist-master.tar.gz distribution
available.

Usage
-----

You can build the image like this

    git clone <this repo>
    cd gitlist-docker
    docker build --rm=true -t gitlist .
    docker build --rm -f Dockerfile -t gitlist-docker:latest .

And run it like this

    docker run --rm=true -p 8888:80 -v /path/repo:/repos gitlist
    docker run --rm=true -p 9999:80 -v D:/Cloud/Git_Nas:/repos gitlist-docker

The web interface will be available on host machine at port 8888 and will show
repositories inside /path/repo
