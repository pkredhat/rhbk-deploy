# RHBK Helm Deployment 

This folder contains the Helm configuration to deploy **Red Hat Build of Keycloak (RHBK)**  Keycloak Helm chart with an overridden Red Hat image.

## Prerequisites
- OpenShift CLI (`oc`)
- Helm 3.x
- A project/namespace created in OpenShift

## Create the secret
oc create secret docker-registry redhat-pull-secret \
  --docker-server=registry.redhat.io \
  --docker-username=<your_RH_account> \
  --docker-password=<your_password> \
  --docker-email=<your_email>

## How to Deploy
- oc new-project rhbk-demo 
- helm upgrade --install rhbk ./rhbk-helm -n rhbk-demo