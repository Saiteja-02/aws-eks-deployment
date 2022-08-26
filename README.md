# aws-eks-deployment
There are two available options for creating a new Kubernetes cluster with nodes in Amazon EKS
  1) eksctl (automatic- command line utility)
  2) aws cli (manual)
  
  # aws cli
    Prerequisites
      1. AWS CLI
      2. kubectl 
      3. Required IAM permissions
      
    Steps:
    
    // Create a cluster
  A. aws cloudformation create-stack \
  --region region-code \
  --stack-name my-eks-vpc-stack \
  --template-url https://s3.us-west-2.amazonaws.com/amazon-eks/cloudformation/2020-10-29/amazon-eks-vpc-private-subnets.yaml
    
    // Create a cluster IAM role
    B.1) Copy the following contents to a file named eks-cluster-role-trust-policy.json
    
    B.2) aws iam create-role \
  --role-name myAmazonEKSClusterRole \
  --assume-role-policy-document file://"eks-cluster-role-trust-policy.json"
  
  
    
    
                    
  
