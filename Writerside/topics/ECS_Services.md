# ECS Services

A Service ensures that a certain number of tasks are running at all times.
![ECS Service](image_6.png)
- Restarts containers that have exited/crashed
- EC2 instance fails, the service will restart task on a working EC2 instance


## Load Balancers

A Load balancer can be assigned to route external traffic to your service.
Even after scaling it will route traffic well
![Load Balancer](image_7.png)