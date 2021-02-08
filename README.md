# Wonderlabs Web Application
Simple load balanced web engine for Wonderlabs. This is merely to demonstrate a static load balanced website that is easily scalable. The application is run on a single AWS EC2 micro node with Docker as follows:

- HaProxy as a load balancer
- 2 x apache web servers

Application can be accessed on http://wonderlabs.letlojanedigital.co.za
Load Balancer stats can be read on http://wonderlabs.letlojanedigital.co.za:1991/ha-stats

## Quick Start
To deploy the application to your Linux instance, please run the following commands in the root directory of this application folder

1. First, initialise the node as docker manager, run ```docker swarm init```
1. Then run ```docker stack deploy --compose-file docker-compose.yaml wonderlabsstack ``` to create your stack defined in the docker-compose file
2. To check if the stack has been created, run ```docker stack ls```
3. Confirm the corresponding containers are running ```docker ps```
