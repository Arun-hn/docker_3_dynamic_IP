It is the continuation of Docker_2 project.
in the docker 2 project we need to change each time hostname ie. public IP of ec2

It is not usefull for automation using docker compose 
so to overcome this we use dynamic IP 
so in index.html I used 
 (async function init() {
        const baseUrl = window.location.origin; // Get the base URL dynamically
        const response = await fetch(`${baseUrl}/get-profile`);
        console.log("response", response);
        const user = await response.json();
        console.log(JSON.stringify(user));

So it can automatically fetch the Public IP 

So build the my app frontend image
docker build -t my-app .

Now run 
docker-compose up

or 
to run the containers in detach mode
docker-compose up -d
