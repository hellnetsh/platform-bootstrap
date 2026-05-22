# Contributing

## Goal
Keep every app repo boring and consistent.

## App repo contract
Each app repo under `hellnetsh` must provide:

```text
repo/
  k8s/
    kustomization.yaml
    namespace.yaml
    deployment.yaml
    service.yaml
    httproute.yaml   # for web apps
```

## Required rules
- repo must live in org `hellnetsh`
- repo must have `k8s/kustomization.yaml`
- app name should match repo name
- namespace should default to repo name
- app must be safe for Argo CD auto-sync

## Tips
- keep manifests minimal
- prefer Kustomize
- use `HTTPRoute` only for web apps
- keep secrets out of git; source them from Vault via ESO

## Naming
- repo: `something-demo`
- app: `something-demo`
- namespace: `something-demo`

## PR checklist
- [ ] `k8s/kustomization.yaml` present
- [ ] manifests apply cleanly
- [ ] app works with Argo CD auto-sync
- [ ] no secrets committed
