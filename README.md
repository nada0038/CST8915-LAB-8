# CST8915 - Lab 8: Full-stack Cloud-native Application Deployment

## YouTube Link:


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



Updated yaml file
