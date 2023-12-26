# boo

Cifrar secrets:

```bash
sops --age=age1wpk6a50fj9hepmve43dtx36fr6rfat6nsms6fx6rf4x2udmmtutsmtzctr --encrypt --encrypted-regex '^(data|stringData)$' --in-place infrastructure/configs/cluster-issuers.yaml
```

k create ns flux-system
kubectl create secret generic sops-age --namespace=flux-system --from-file=age.agekey=age.agekey
flux bootstrap github --token-auth --owner=fabianonunes --repository=flux2-kustomize-helm-example --branch=main --personal --path=clusters/production
