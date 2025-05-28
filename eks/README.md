First install the cluster using eksctl
```
eksctl create cluster -f cluster.yaml
```
Next configure your kubeconfig file
```
aws eks update-kubeconfig --region us-east-1 --name cluster-dkh
```
Then install a load-balancer controller using Helm (much easier with auto-mode btw)
```
helm repo add eks https://aws.github.io/eks-charts

helm repo update eks

helm install aws-load-balancer-controller eks/aws-load-balancer-controller \  
  -n kube-system \  
  --set clusterName=cluster-dkh \  
  --set serviceAccount.create=false \  
  --set serviceAccount.name=aws-load-balancer-controller \  
  --version 2.13.2  
```

