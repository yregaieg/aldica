# Introduction
The Kubernetes installation utilizes the upstream [Alfresco Content Services Community Deployment](https://github.com/Alfresco/acs-community-deployment) [Helm](https://helm.sh/) chart.

# Prerequistes
* Kubernetes cluster with Ingress

# Installation
* Fetch the latest Helm chart release from [acs-community-deployment](https://github.com/Alfresco/acs-community-deployment/releases/latest)
* Extract the archive and navigate to the `helm/alfresco-content-services-community/` folder (the folder containing the Chart.yaml file).
* Apply the provided patch file, by running:
```
patch ...
```
* Build Docker image
* Install according to README.md in Helm chart folder.



