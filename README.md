# Hurdle Archive GitOps

This repository contains the in-cluster configuration. Using ArgoCD’s app-of-apps pattern, I declaratively manage and continuously deploy the Hurdle Archive application and its associated infrastructure. ArgoCD, pre-installed in the cluster, continuously monitors the applications and reconciles their state with the desired configurations specified in this repository.

### Managed Applications

- Hurdle Archive application (along with a MySQL database)
- Nginx Ingress Controller
- Cert-Manager application (for TLS encryption)
- Prometheus and Grafana (KPS stack for monitoring)
- Elasticsearch, Fluent-bit, and Kibana (EFK stack for logging)

## Cluster Diagram

![Cluster_Diagram.png](./docs/Cluster_Diagram.png "Cluster Diagram")

## Context

The Hurdle Archive app, along with its Docker packaging and Jenkins CI/CD pipeline can be found [here](https://github.com/nlemberg/hurdle-archive).
Provisioning of the infrastructure components in AWS using Terraform code can be found in [this repo](https://github.com/nlemberg/hurdle-archive-infra)
