# Elastic Container Service-
- Amazon ECS is a fully managed container orchestration service by AWS.
- It helps you run Docker containers at scale without manually managing container scheduling, scaling, and networking.
- ECS integrates deeply with AWS services like IAM, CloudWatch, VPC, ALB/ELB, ECR.

# EC2 Launch Type -
- You create an ECS Cluster with EC2 instances.
- Containers (tasks) run on those EC2 instances.
# Fargate Launch Type -
- Serverless option → No EC2 to manage.
- You only define:
    - CPU & Memory per task
    - Docker image to run

- AWS provisions the compute resources on-demand and scales automatically.
- You pay only for vCPU and memory per second while the container is running.

# ECS Architecture-
## a) ECS Cluster
- A logical grouping of compute resources where your containers run.

## b)Task Definition-
- A blueprint (JSON file) describing how to run your container.
- Includes:
    - Docker image 
    - CPU and Memory required
    - Networking (ports, environment variables)
    - Volumes (if any)
## c) Task-
- A running container instance based on the Task Definition.

## d) Service -
- Ensures a specified number of tasks keep running.
- Can connect tasks to:
Application Load Balancer (ALB)
Network Load Balancer (NLB)
