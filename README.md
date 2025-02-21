## Kubernetes Demo 
Varied sample Kubernetes manifests are provided for use in deployments of Kubernetes clusters with Kind, utilizing Kustomize or Helm package manager: \
**Kustomize:** for managing overlays and customization of existing clusters with YAML files and `kubectl`. \
**Helm:** for deploying new clusters using Helm Charts.

Deplyments are done through CICD or yet better GitOps:\
**CICD:** CI is done with Github Actions and CD is done using deployment yaml and kubectl. This is a traditional method but not ideal since the deployment process is run each time we push or tag. \
**GitOps:** CI is done with Github Actions and CD is done with GitOps practice using tools like ArgoCD. This is ideal since we synchronize to git repo as the single source of truth and we have the option to rollback to different versions and adjust by pulling from git and many other benefits. \
![Version](https://img.shields.io/badge/version-1.0.2-green)  


### Prerequisites

- Docker
- Kind (Kubernetes in Docker)
- Kubectl
