# Hello GitOps

Example project to demonstrate GitOps using `GitHub Actions`, `OpenShift`, `Kustomize`, and `ArgoCD`: 

- [What we want to achieve](#what-we-want-to-achieve)
- [Setup GitHub]
- [Configure GitrHub Actions]
- [Test the application]
  
## What we want to achieve

1. Code change is made to a Go application and pushed to master
1. GitHub Actions workflow is triggered
1. Code is first unit tested
1. If tests are OK, the application is packaged as a Docker image and pushed to DockerHub
1. The kustomize manifests are edited to reference this new image tag
1. Kustomize changes are committed and pushed automatically by the workflow
1. As kustomize files have changed, ArgoCD synchronize the application state with the OpenShift Kubernetes cluster to deploy or update the app


