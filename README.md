#### egcompose
This repository contains docker-compose and related files to set up Express Gateway in a single step.

##### Simple Deployment
The current folder contains a docker-compose file and other required files for a one-step set up of Express Gateway with Redis.

Just run : docker-compose up -d

This will start an Express Gateway container and a linked Redis container. Commonly used ports are exposed.

The docker compose script overlays the gateway and system config files with example configuration files in the same directory. For your usage replace these files with you own. For example gateway config includes an API endpoint to find out the current IP address of the client.

##### Advanced Deployment
To set up Express Gateway in a manner that is closer to a production deployment, navigate to the production sub-directory.

Then, copy a key and certificate file to this directory named ssl.key and ssl.crt respectively, to the production sub-directory, to support HTTPS.

Then run: docker-compose up -d

This sets up Express Gateway with Redis sentinel and HTTPS support. 

For detailed steps, please refer to:  
[One-Step Dev Setup for Express Gateway Using egcompose](http://techyugadi.com/express_gateway_egcompose_1.html)  
[Express Gateway Set-up Using egcompose With Redis Sentinel and HTTPS](http://techyugadi.com/express_gateway_egcompose_2.html)

The better approach is to use a [Kubernetes-based deployment](https://github.com/DrMegavolt/k8s-redis-ha/blob/master/example/express-gateway.yml) , but this is for a quick setup in a dev environment.
