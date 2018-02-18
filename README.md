# docker-stack-ibm

Just comment unnecessary containers.

You can use [openldap](https://hub.docker.com/r/osixia/openldap/) instead of apacheds.  

Next steps:
1. new branch to deploy some applications.
1. new branch to configure HADR.
1. new branch with Dynatrace [for example](https://github.com/dynatrace-innovationlab/easyTravel-Docker/blob/master/docker-compose-withDtAppMon.yml).

Following containers are missing (For licensing reasons):
* The WebSphere Application Server Network Deployment (dmgr)

https://developer.ibm.com/recipes/tutorials/how-to-configure-ibm-websphere-application-server-network-deployment-cell-topology-using-docker-containers/
* The WebSphere Portal server

https://developer.ibm.com/digexp/docs/docs/customization-administration/ibm-digital-experience-on-docker-containers/

## Tools
* MQ:
MQ explorer, rfhutil or HermesJMS 
* LDAP: 
[jxplorer](http://jxplorer.org/index.html)
* WAS: 
*TODO: find a librarie to deploy applications, create resources, ...*
* DB2: [SQuirreL](https://www.ibm.com/developerworks/data/library/techarticle/dm-0312bhogal/index.html)

## docker commands

    To start all servers: docker-compose up -d. 
    To see logs: docker-compose logs
    To stop all servers: docker-compose stop
    To check resources used: docker stats
    To delete containers: docker-compose rm
    To remove images: docker ps -a | awk '{print $1}' | xargs --no-run-if-empty docker rm
    Delete all containers docker rm $(docker ps -a -q)
    Delete all images docker rmi $(docker images -q)


## websphere-liberty
Interesting links:

https://hub.docker.com/r/library/websphere-liberty/

https://developer.ibm.com/wasdev/docs/deploying-a-web-application-using-liberty-db2-docker-swarm-and-docker-compose-across-multiple-docker-machines/

https://developer.ibm.com/wasdev/docs/using-docker-compose-configure-topology-websphere-liberty-ibm-mq/

