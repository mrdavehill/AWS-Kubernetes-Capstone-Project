```
eksctl create cluster -f cluster.yaml

aws eks update-kubeconfig --region us-east-1 --name cluster-dkh
```
Then install a load-balancer controller using Helm (much easier with auto-mode btw)


