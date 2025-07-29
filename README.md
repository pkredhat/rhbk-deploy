# RHBK Helm Deployment (Bitnami Chart Override)

This folder contains the Helm configuration to deploy **Red Hat Build of Keycloak (RHBK)**  Keycloak Helm chart with an overridden Red Hat image.

## Prerequisites
- OpenShift CLI (`oc`)
- Helm 3.x
- A project/namespace created in OpenShift

## How to Deploy
oc new-project rhbk-demo
helm upgrade --install rhbk ./rhbk-helm -n rhbk-demo