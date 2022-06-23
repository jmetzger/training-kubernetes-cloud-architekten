# Wichtige kubectl kommandos 

## Allgemein 

```
# Zeige Information über das Cluster 
kubectl cluster-info 

# Welche api-resources gibt es ?
kubectl api-resources 
kubectl api-resources | grep namespaces 

# Hilfe zu object und eigenschaften bekommen
kubectl explain pod 
kubectl explain pod.metadata
kubectl explain pod.metadata.name 

```

## Namespace im context ändern 

```
# mein default namespace soll ein anderer sein, z.B eines Projekt
kubectl config set-context --current --namespace=tln2 

```

## Hauptkommandos 

```
kubectl get 
kubectl delete 
kubectl create
```


## namespaces 

```
kubectl get ns
kubectl get namespaces 

```

## Arbeiten mit manifesten 

```
kubectl apply -f nginx-replicaset.yml 
# Wie ist aktuell die hinterlegte config im system
kubectl get -o yaml -f nginx-replicaset.yml 

# Änderung in nginx-replicaset.yml z.B. replicas: 4 
# dry-run - was wird geändert 
kubectl diff -f nginx-replicaset.yml 

# anwenden 
kubectl apply -f nginx-replicaset.yml 

# Alle Objekte aus manifest löschen
kubectl delete -f nginx-replicaset.yml 


```

## Ausgabeformate / Spezielle Informationen

```
# Ausgabe kann in verschiedenen Formaten erfolgen 
kubectl get pods -o wide # weitere informationen 
# im json format
kubectl get pods -o json 

# spezielle Eigenschaften zurückgeben 
kubectl get pods nginx-static-web -o jsonpath='{.metadata.namespace}'

# gilt natürluch auch für andere kommandos
kubectl get deploy -o json 
kubectl get deploy -o yaml 

# Label anzeigen 
kubectl get deploy --show-labels 

```



## Zu den Pods 

```
# Start einen pod // BESSER: direkt manifest verwenden
# kubectl run podname image=imagename 
kubectl run nginx image=nginx 

# Pods anzeigen 
kubectl get pods 
kubectl get pod

# Pods in allen namespaces anzeigen 
kubectl get pods -A 

# Format weitere Information 
kubectl get pod -o wide 
# Zeige labels der Pods
kubectl get pods --show-labels 

# Zeige pods mit einem bestimmten label 
kubectl get pods -l app=nginx 

# Status eines Pods anzeigen 
kubectl describe pod nginx 

# Pod löschen 
kubectl delete pod nginx 

# Kommando in pod ausführen 
kubectl exec -it nginx -- bash 

```

## Arbeiten mit namespaces 

```
# Welche namespaces auf dem System 
kubectl get ns 
kubectl get namespaces 
# Standardmäßig wird immer der default namespace verwendet 
# wenn man kommandos aufruft 
kubectl get deployments 

# Möchte ich z.B. deployment vom kube-system (installation) aufrufen, 
# kann ich den namespace angeben
kubectl get deployments --namespace=kube-system 
kubectl get deployments -n kube-system 
```

## Alle Objekte anzeigen 

```
# Manchen Objekte werden mit all angezeigt 
kubectl get all 
kubectl get all,configmaps 

# Über alle Namespaces hinweg 
kubectl get all -A 


```

## Logs

```
kubectl logs <container>
kubectl logs <deployment>
# e.g. 
# kubectl logs -n namespace8 deploy/nginx
# with timestamp 
kubectl logs --timestamp -n namespace8 deploy/nginx
# continously show output 
kubectl logs -f <container>
```

## Debugging hochsetzen für kubectl 

```
# höchstes Loglevel 9 
kubectl -v=8 get pods nginx-static-web -o jsonpath='{.metadata.namespace}'
```

## Referenz

  * https://kubernetes.io/de/docs/reference/kubectl/cheatsheet/
