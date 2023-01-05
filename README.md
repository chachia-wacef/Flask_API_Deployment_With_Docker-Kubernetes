# Flask_API_Deployment_With_Docker-Kubernetes

In this project I deployed a simple application programming interface with Flask python using the Devops tools Docker and Kubernetes.

The goal of this deployment is to create 3 instances of our application and to use a load balancer to distribute the incoming traffic to our service and guarantee its availability over time.

The steps of this project are the following: 

* 1- Develop an API with Flask python and test it locally.
<img src="./Project_screenshots/0.png" alt="Flask API" width="500" height="100">

* 2- We create the dockerfile API to build the docker image.
* 3- Run $docker build -t wacef-flask-api . ==> the docker image is generated (check with $docker images)
<img src="Project_screenshots/1.png" alt="Build Docker image" width="500" height="100">

<img src="Project_screenshots/3.png" alt="Docker images" width="500" height="100">

* 4- $kubectl apply -f deployment.yaml ==> We create our deployment with kubernetes.
<img src="Project_screenshots/4.png" alt="Build Docker image" width="500" height="100">

* 5- $minikube dashboard ==> Check the status of the components of our deployment on the kubernetes dashboard.
<img src="Project_screenshots/5.png" alt="Deployment status (1)" width="500" height="100">
<br>
<img src="Project_screenshots/6.png" alt="Deployment status (2)" width="500" height="100">
<br>
<img src="Project_screenshots/7.png" alt="Deployment status (3)" width="500" height="100">

* 6- $minikube service flask-wacef-service ==> Access our deployed api and make sure it works.
<img src="Project_screenshots/8.png" alt="Deployment service start" width="500" height="100">
