docker-api
==========

##Api rest with express and docker

### Requirements:
	
####We have install docker and fig

Install docker 

	https://docs.docker.com/installation/#installation

Ubuntu
	
	sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 36A1D7869245C8950F966E92D8576A8BA88D21E9

	$ sudo sh -c "echo deb http://get.docker.io/ubuntu docker main\> /etc/apt/sources.list.d/docker.list"

	$ sudo docker run -i -t ubuntu /bin/bash

Arch Linux
	
	$ pacman -S docker

	starting docker

More distributions
	
	https://docs.docker.com/installation/


Install fig 

Linux
	
	$ curl -L https://github.com/docker/fig/releases/download/0.5.2/linux > /usr/local/bin/fig
	$ chmod +x /usr/local/bin/fig
	


####Clone repository

	git clone repisotory https://github.com/marcko/docker-api.git



####Create data container for Mongodb


	docker run -v /data/db --name MONGODB_DATA busybox true

#### Create directory for logs


	sudo mkdir -p /var/log/docker/docker-api


####Run app

	fig up -d