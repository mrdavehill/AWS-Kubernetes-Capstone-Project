eksctl create cluster -f cluster.yaml

aws eks update-kubeconfig --region us-east-1 --name cluster-dkh
