# platform-bootstrap

Bootstrap repo for Argo CD IDP.

## Contains
- `AppProject` for the `hellnetsh` org
- `ApplicationSet` that discovers repos with `k8s/kustomization.yaml`

## Convention
- each app repo must expose Kubernetes manifests under `k8s/`
