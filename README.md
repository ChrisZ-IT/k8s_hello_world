# k8s_hello_world
hello world project while I learn k8s

## Requirements
- You will need to ensure your K8s cluster has networking setup as well as is able to use the loadbalancers service type. This project was tested using calico and metalLB not running in the cloud
  - [base calico and MetalLB setup](https://github.com/ChrisZ-IT/base_k8s_deployment)


### Deployment
  - Run `kubectl apply -f k8s_hello_world/Deployment/deployment.yml` to deploy base hello_world pods
    - Ensure these pods are get into a running state `kubectl get pods hello-world
  - Run `kubectl apply -f k8s_hello_world/Service/service.yml` to create the loadbalancer service
    - run `kubectl get service hello-world` and ensure it has an `EXTERNAL-IP`
  - Open your browser and enter that external-ip.
    - You should see a hello-world test page and the hostname listed on that site should match the names on your hello-world pod(s) when


# to-do
  - Get ssl/tls working for https