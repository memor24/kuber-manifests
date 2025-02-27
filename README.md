## Kubernetes Demo 
![Version](https://img.shields.io/badge/version-1.2.4-green)  


Varied practical Kubernetes manifests are provided for use in deployments of Kubernetes clusters.

**Helm:** for deploying new clusters using Helm Charts. \
**Kustomize:** for managing overlays and customization of existing clusters with YAML files and `kubectl`.


Deployments can be done through CICD or yet better GitOps: \
**CICD:** CI is done with Github Actions and CD is done using deployment.yaml and kubectl via Github Actions pipeline or any other CICD tool. This is a traditional method but not ideal since the deployment process is run each time we push or tag. There will be no visibility into the cluster until test cases are done, not to mention a lot access control requirments (to kubectl, cicd tools, cloud providers, etc) which compromises security and the principle of least privilleges.\
**GitOps:** CI is done with Github Actions and CD is done with GitOps practice using tools like ArgoCD. This is ideal since the app is consistently synchronized with the git repo as the single source of truth and we have the option to rollback to different versions by pulling from git, and many other benefits.

### Prerequisites

- Docker
- Kind (Kubernetes in Docker)
- Kubectl

Helm package manager can also be used to auto generate base manifests as Helm Chart to be edited and used. \
```
helm create myapp
```
