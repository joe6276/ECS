# ECS

ECS is a managed container orchestrator

![Orchestrators](image.png)

## Why Orchestrator

- It manages the lifecycle of containers creates /restart/ destroy
- Deploy and load-balance application across multiple servers
- Autoscaling to handle variance in traffic
- Rolling-out changes to application

### ECS Vs Others
Without an Orchestrator, if using docker run or docker compose, and you run application, 
you can only deploy it to one server
![Docker Compose Deployment](image_1.png)

You can technically copy to the other servers, but none of the other servers
are aware that the same app is running on any other server.
The orchestrator should be intelligent to scale up and down on their own.

## Why ECS
![ECS VS Others ](image_2.png)



## ECS Infrastructure and Launch
ES has two launch types:
- EC2 (this is a Compute service that runs servers)
- Fargate (Serverless) 

But before this lets understand a cluster.
### Cluster
<tip>
ECS is just the brain behind how the containers are deployed.
It only works with containers
ECS has no servers
ECS has no compute power
</tip>

ECS creates and deletes container, but it 
still needs underlying infrastructure to run those containers on.That's a **Cluster** is just a 
bunch of resources that the container is going to run on 

### EC2 Launch Type

- With the EC2 launch type, we have to manage the underlying EC2 instances.
- You still need to manage the underlying infrastructure (EC2)
- ECS will manage the containers
- You have full control over your infrastructure
- You have to install docker, patches, ECS Agent, firewall, etc.
![EC2 Launch Type](image_3.png)

### ECS Fargate 
- Here AWS manages the underlying infrastructure 
- Follows a serverless architecture
- ECS will talk to fargate and fargate will create servers on demand
- ECS will now deploy the container into the existing infrastructure
- No need to provision/ maintain EC2 servers.
- You pay for what you use

 

