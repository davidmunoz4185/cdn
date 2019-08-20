# Cloud DevOps NanoDegree - Capstone Project

### Summary ...

Last project for Cloud DevOps Nanodegree. In this project we create a EKS Cluster by terraform and deploy an app into it.

### How to ...

``` script
terraform apply
aws eks update-kubeconfig --name terraform-eks-dmm
kubectl apply -f config_map_aws_auth.yaml
kubectl apply -f rbac-role.yaml
kubectl apply -f alb-ingress-controller.yaml
kubectl apply -f dmm-deployment.yaml
kubectl apply -f dmm-service.yaml
kubectl apply -f dmm-ingress.yaml

```
