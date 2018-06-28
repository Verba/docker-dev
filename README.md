# Dev Tools

This is a docker compose file that gives you a Redis and Memcached so that 
you don't have to install them locally. We can add other tools to make
bootstrapping new projects easier. 

  1. Get docker going. See the interwebs for the latest documentation.
  2. Make sure you have a local machine called `default`
  3. `docker-compose up`
  
  
  
# Images

Images that we use across projects

## circleci

Image to run commands on circleci with the basic circleci setup.

Published as `verba / circleci-node-awsebcli`

Push new one as `docker push verba/circleci-node-awsebcli:tagname`



# Helpful Docker Commands & Links

Currently out images are hosted on [Docker Cloud](https://cloud.docker.com/swarm/verba/repository/list).

To run a command in an ubunti instance:
```bash
docker run -w /usr/src/app node:8 /bin/bash -c '<the command>'
```

To run a command in an ubunti instance with the current directory mounted:
```bash
docker run -w /usr/src/app -v "$(pwd)":/usr/src/app node:8 /bin/bash -c 'yarn install && yarn build'
```