# Questions and Answerts 

## Wieviele Replicaset beim Deployment zurückbehalt / Löschen von Replicaset 

```

kubectl explain deployment.spec.revisionHistoryLimit 

apiVersion: apps/v1
kind: Deployment
# ...
spec:
  # ...
  revisionHistoryLimit: 0 # Default to 10 if not specified
  # ...
  
```

## Wo dokumentieren, z.B. aus welchem Repo / git 

  * https://kubernetes.io/docs/concepts/overview/working-with-objects/common-labels/