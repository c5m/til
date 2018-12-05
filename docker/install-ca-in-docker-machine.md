# Install CA in docker-machine
To install your own CA in a `docker-machine` image do the following:
~~~
docker-machine ssh default 'sudo mkdir /var/lib/boot2docker/certs'
docker-machine scp corp-ca.pem default:
docker-machine ssh default 'sudo mv corp-ca.pem /var/lib/boot2docker/certs/'
docker-machine restart default 
~~~