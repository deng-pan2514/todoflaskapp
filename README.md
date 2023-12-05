# todoflaskapp
assignment3 for cloud computing &amp; big data 6998

**Part 1: Creating an Application**:

**Part 2:** **Containerizing the Application using Docker**:

**Part 3: Deploying the Application on Minikube**:

**Part 4: Deploying the Application on AWS EKS**:

**Part 5: Replication controller feature**:

**Part 6: Rolling update strategy**:

**Part 7: Health monitoring**:

**Part 8: Alerting**:

**Setup Prometheus:**

kubectl create namespace monitoring

kubectl create -f clusterRole.yaml

kubectl create -f config-map-v1.yaml

kubectl create  -f prometheus-deployment.yaml

kubectl get deployments --namespace=monitoring

kubectl create -f prometheus-service.yaml --namespace=monitoring

**Setup Kube State Metrics:**

kubectl apply -f kube-state-metrics-configs/

kubectl get deployments kube-state-metrics -n kube-system

**Setup AlertManager:**

kubectl create -f AlertManagerConfigmap.yaml

kubectl create -f AlertTemplateConfigMap.yaml

kubectl create -f alertmanagerdeployment.yaml

kubectl create -f alertmanagerservice.yaml

