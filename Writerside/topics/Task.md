# ECS Task Definition

After a user writes a docker file, then build an image, and you can now push the image to Dockerhub.
![ECS](image_4.png)

- A Task definition is a blueprint that describes how containers should launch
- Contains the container definition of how much CPU and Memory, Images, Ports and Volume to use.
- Contains all the configurations a docker compose file has.
- You can describe all containers on one task definition or even on different definition.

## Task
- A task is an instance of a task definition.
- A running container(s) with settings defined in the task definition.

![Task ](image_5.png)