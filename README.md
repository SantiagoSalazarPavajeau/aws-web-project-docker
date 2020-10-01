Add configuration files (.ebextensions), Procfile and Dockerrun.aws.json and then create an Elastic Beanstalk instance through CLI commands.

Some cli commands:

```
eb create --single
eb deploy
```

ECR Setup:

- Add IAM role in AmazonEC2ContainerServiceforEC2Role: esaInstanceRole, ElasticContainerServiceTask

- Create cluster in ECS: Linux, On-demand, t2.micro, 1 instance.

- Create Task Definition (EC2) : 500MB, 1 vcpu, add container, add image repo,memory, PORTS

- Create Service from ECSCluster: puts a task on the EC2 instance
 
- Run ECS task to have the application launched.