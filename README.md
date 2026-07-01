# Admin Gate

Petit site statique kawaii pour la question : "Veux-tu être mon admin ?".

## Build local

```bash
docker build -t admin-gate .
docker run --rm -p 8080:80 admin-gate
```

Puis ouvrir <http://localhost:8080>.

## Kubernetes / ArgoCD

Les manifests sont dans `k8s/` et peuvent être ciblés par ArgoCD avec Kustomize.

L'image par défaut est :

```text
ghcr.io/tenshi-lab-kube/admin-gate:main
```

À adapter si ton pipeline de build pousse l'image ailleurs.

Le service Kubernetes exposé en interne est `admin-gate.admin-gate.svc.cluster.local:80`.
