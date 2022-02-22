# Capstone_Project

![image](https://user-images.githubusercontent.com/60229601/154626757-54439171-8251-4a9c-a35d-6a985810e6c3.png)

# Cluster creation and initialization

Used eksctl version 0.83.0 for creating Kubernetes Cluster

      Config yaml file - ./kube/cluster.yaml

      Command => eksctl create cluster -f cluster.yaml

Configured IAM role for the Kubernetes Cluster

      eksctl get iamidentitymapping --cluster mycluster
      
      eksctl create iamidentitymapping --cluster  mycluster --arn arn:aws:iam::106876110629:role/eksctl-mycluster-cluster-ServiceRole-TW8D1GYOMCIB --group system:masters --username Admin

# Scope: -

=> Create a kubernetes cluster.

=> Creat Docker images of the application and push them to the Docker hub.

=> Use Rolling deployment strategy to move from old to new version of the App.

=> Use CIRCLECI for creating the CICD pipeline.

=> Capture the linting error.


Environment Variables used: - 

AWS_ACCESS_KEY_ID

AWS_SECRET_ACCESS_KEY

AWS_DEFAULT_REGION

DOCKERHUB_PASSWORD
