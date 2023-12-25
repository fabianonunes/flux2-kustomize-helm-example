# boo

Cifrar secrets:

```bash
sops --age=age1wpk6a50fj9hepmve43dtx36fr6rfat6nsms6fx6rf4x2udmmtutsmtzctr --encrypt --encrypted-regex '^(data|stringData)$' --in-place infrastructure/configs/cluster-issuers.yaml
```
