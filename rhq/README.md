RHQ dockerized
====

Ready to use, SSH enabled [RHQ 4.11](http://rhq.jboss.org/) docker image


Requirement
---
Docker 1.x


Usage
---
To run RHQ, run the script [launch.sh](https://github.com/gustavonalle/docker/blob/master/rhq/launch.sh), it will print the IP adress of the RHQ server

After that, point the browser to http://address:7080/ and login using 'rhqadmin' as user and password

SSH is open, root password is 'root'


Details
---

RHQ runs on top of Postgresql, Fedora 20 and Java 1.7. 

Services (SSH, PostgreSQL, RHQ Agent, Storage Node, Agent) are managed by [Supervisor](http://supervisord.org)

Docker registry
---

The image is being build on the docker regsitry at [gustavonalle/rhq-411-server](https://registry.hub.docker.com/u/gustavonalle/rhq-411-server/)
