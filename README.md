# CST8915 - Lab 8: Full-stack Cloud-native Application Deployment

## YouTube Link:
https://youtu.be/79ZFCHvbyCQ

## Updated yaml file
https://github.com/nada0038/CST8915-LAB-8/blob/main/aps-all-in-one.yaml

## Explanation
I added persistent storage and enabled high availability to enhance the MongoDB and RabbitMQ deployments. In order to enable reliable DNS domains needed for replica-set operation, MongoDB was converted to a StatefulSet with several replicas, each utilising its own PersistentVolumeClaim. Additionally, the service was made headless. Mounting a PersistentVolume at /var/lib/rabbitmq improved RabbitMQ by preventing queues and messages from being lost during pod restarts. Both services are now robust and fault-tolerant thanks to these modifications. Additionally, I found that Azure Cosmos DB (MongoDB API) and Azure Service Bus are fully managed cloud substitutes that offer inherent dependability without requiring Kubernetes to support stateful workloads.


### Services Deployed

The following services are deployed and running:

| Service                | Status   | Notes |
|------------------------|---------|-------|
| store-front            | Running | Frontend application |
| store-admin            | Running | Admin application |
| order-service          | Running | Backend order service |
| product-service        | Running | Backend product service |
| virtual-customer       | Running | Simulated customer service |
| virtual-worker         | Running | Simulated worker service |
| rabbitmq-0             | Running | Messaging service |
| mongodb                | Running | Database service |


## Access

- **Store Frontend:** [http://64.236.250.96] 
- **Store Admin:** [http://23.96.223.181]  


## Docker Images

All images were built and pushed to Docker Hub under the username **`nada0038`**:

| Service                | Image |
|------------------------|-------|
| store-front            | nada0038/store-front:v1 |
| store-admin            | nada0038/store-admin:v1 |
| order-service          | nada0038/order-service:v1 |
| product-service        | nada0038/product-service:v1 |
| virtual-customer       | nada0038/virtual-customer:v1 |
| virtual-worker         | nada0038/virtual-worker:v1 |
| rabbitmq               | rabbitmq:3.11-management |
| mongodb                | mongo:6.0 |



