#### egcompose

A docker-compose file and other required files for a one-step set up of Express Gateway with Redis.

Just run : docker-compose up -d

This will start an Express Gateway container and a linked Redis container. Commonly used ports are exposed.

The docker compose script overlays the gateway and system config files with example configuration files in the same directory. For your usage replace these files with you own. For example gateway config includes an API endpoint to find out the current IP address of the client.

TO DO:
i. use redis sentinel
ii. allow copying of ssl certificates for HTTPS support
