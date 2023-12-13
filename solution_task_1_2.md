
# Solution (Task-2)
- The Dockerfile for the apps red, yellow, green are in their respective directories
- The Dockerfile for the nginx-proxy image is in the nginx directory
- ##### To create network 
- docker network create --subnet=172.20.0.0/16 --gateway=172.20.0.1 traffic-light
- ##### Docker run commands
- docker run --rm --network traffic-light --name green-app trafficlight/green:v1.0
- docker run --rm --network traffic-light --name red-app trafficlight/red:v1.0
- docker rrn --rm --network traffic-light --name yellow-app trafficlight/yellow:v1.0
- docker run --rm -p 80:80 -p 3000:3000 -p 4000:4000 -p 5000:5000 --network traffic-light --name nginx-proxy trafficlight/nginx:v1.0
- - NOTE: Mac users may need to disable the Airplay Receiver as it by default runs on port 5000
