# aws-ecs-workshop-1_deploy_microservices_to_ecs
In this workshop, we will launch a frontend and multiple backend services on Amazon Elastic Container Service, and explore how you might adopt this workflow into your environment. This workshop is based on  "AWS ECS Workshop - Deploying Microservices to ECS" (https://ecsworkshop.com/microservices/). 

In total, there are 4 services that we will build. All of them are implemented using ECS Fargate. 
- platform (basic infrastructure like load balancer, vpc, iam permission)
- frontend powered by ruby on rails
- backend powered by nodejs
- backend powered by crystal

What the platform looks like.
![platform architecture](https://ecsworkshop.com/images/mu-topology-vpc.png)

On top of the platform above, the rest of services are built so that they have diagram like below.
![service diagram](https://ecsworkshop.com/images/3-tier-architecture.svg)


To deploy the ECS Fargate, we can either use AWS Copilot (cli tool to work with ECS) or AWS Cloud Development Kit/CDK (an SDK that act as wrapper of CloudFormation). In this repo, both of the source code for Copilot and CDK are included. However, in this workshop, I use the Copilot.
