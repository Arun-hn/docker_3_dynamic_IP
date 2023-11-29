It is the continuation of Docker_1 project.
Here we use Docker-compose.yml file to run containers.

Before running docker-compose.yaml
first run 
change host to ec2-public-ip in index.html and 

docker build -t my-app .

then my-app image built,


Now run 
docker-compose up

or 
to run the containers in detach mode
docker-compose up -d
