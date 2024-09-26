# Kubernetes Configuration Repository

## Overview

This repository contains the Kubernetes configuration files for managing API and Frontend services within an Amazon EKS cluster. It includes `Deployment` and `Service` configurations for each service, as well as a shared `Ingress` configuration to route traffic to the appropriate service.

## Structure

- `api/`: Contains the deployment and service manifests for the API service.
- `frontend/`: Contains the deployment and service manifests for the Frontend service.
- `ingress/`: Contains the ingress configuration to route traffic for both services.

## How to Use

Apply the configurations using `kubectl`:

```bash
kubectl apply -f api/api-deployment.yml
kubectl apply -f api/api-service.yml
kubectl apply -f frontend/frontend-deployment.yml
kubectl apply -f frontend/frontend-service.yml
kubectl apply -f ingress/ingress.yml
```

## Ingress Configuration
The ingress configuration uses the AWS Load Balancer Controller to create an ALB (Application Load Balancer) and route traffic to the services.

- API: `/api`
- Frontend: `/`
- 
## License

Licensed under the MIT License. See the LICENSE file for more details.
