# Kubernetes Praxis für Cloud Architekten

## Agenda 

  1. Einführung Container-Architektur
     * [Warum Kubernetes?](warum-kubernetes.md)
     * [Kubernetes-Cluster-Architektur](/kubernetes/architecture.md)
     * [OpenShift 4 vs. Kubernetes (Vanilla)](/kubernetes/openshift4-vs-kubernetes.md)

  1. Installation
     * [Client (Windows)](/kubernetes/installation-client-windows.md)
     
  1. kubectl 
     * [Spickzettel](/kubectl/spickzettel.md)
     * [bash completion](/kubectl/bash-completion.md)


  1. Kubernetes Komponenten & Objekte (Teil 1) 
     * [Pods - by example](/kubectl-examples/01-pod-nginx.md)
     * [ReplicaSets - by example](/kubectl-examples/01a-replicaset-nginx.md)
     * [Deployments - by example](/kubectl-examples/03-nginx-deployment.md)
     * [Services - by example](/kubectl-examples/03b-service.md)
     * Jobs
     * DaemonSets
  
  1. Kubernetes Komponenten (Teil 2: Der Klebstoff) 
     * [Labels and Annotations]()
	
  1. Kubernetes Komponenten (Teil 3: Arbeiten mit Konfigurationen)
     * [Config Maps]()
     * [Secrets]()
     * [SealedSecrets]()
  
  1. Anwendungen (Teil 1: Allgemein)
     * Anwendungsskalierung & Load Balancing
     * Rolling Updates
     * Service Discovery 
     * Volumes & Storage

  1. Anwendungen (Teil 2: Network and Container-Security) 
     * Network Security 
     * Container Security 

  1. Infrastructure as Code (IaC) 
     * Kubernetes Configuration Files 
     * Helm Package Manager  

  1. CI/CD (Überblick) 

  1. Monitoring and Logging
     * Prometheus & Grafana

  1. Wrap-up, Q&A und Ausblick
     * Muss es immer Kubernetes sein?
     * Was ist Kuberentes und was ist OpenShift 
     * Function as a Service

## Backlog 
  
  1. Kubernetes (Refresher) 
     * Kubernetes und seine Objekte (pods, replicasets, deployments, services, ingress) 
     * Verbinde mit kubectl 
     * Manifeste ausrollen (im Namespace) (2-3)
     * Arbeiten mit non-root images 

  1. Kubernetes Praxis API-Objekte 
     * [Das Tool kubectl (Devs/Ops)](/kubectl/spickzettel.md)
     * [kubectl example with run](/kubectl/run-with-example.md)
     * Arbeiten mit manifests (Devs/Ops)
     * Pods (Devs/Ops)
     * [kubectl/manifest/pod](/kubectl-examples/01-pod-nginx.md)
     * ReplicaSets (Theorie) - (Devs/Ops)
     * [kubectl/manifest/replicaset](/kubectl-examples/01a-replicaset-nginx.md)
     * Deployments (Devs/Ops)
     * [kubectl/manifest/deployments](/kubectl-examples/03-nginx-deployment.md)
     * Services (Devs/Ops)
     * [kubectl/manifest/service](/kubectl-examples/03b-service.md)
     * DaemonSets (Devs/Ops)
     * IngressController (Devs/Ops)
     * [Hintergrund Ingress](/kubernetes/ingress.md) 
     * [Documentation for default ingress nginx](https://kubernetes.github.io/ingress-nginx/user-guide/nginx-configuration/configmap/)
     * [Beispiel mit Hostnamen](/kubectl-examples/04-ingress-nginx-with-hostnames.md)

  1. Kubernetes Secrets / Sealed Secrets (bitnami) 
     * [Welche Arten von secrets gibt es?](/kubernetes/secrets/secrets.md)
     * [Übung mit secrets](/kubernetes/uebungen-secrets.md)
     * [Übung mit sealed-secrets](/kubernetes/secrets/sealed-secrets.md)

  1. Kubernetes Probes (Liveness and Readiness) 
     * [Übung Liveness-Probe](/probes/uebung-liveness.md)
     * [Funktionsweise Readiness-Probe vs. Liveness-Probe](/probes/readiness.md) 
  
  1. Kubernetes Wartung / Fehleranalyse
     * [Wartung mit drain / uncordon (Ops)](/kubectl/uncordon-drain.md) 
     * [Debugging Ingress](/kubernetes/debugging-ingress.md) 

  1. Kubernetes Pods Disruption Budget 
     * [PDB - Uebung](/kubernetes/pdb/uebung.md)

  1. Kubernetes PodAffinity/PodAntiAffinity
     * [Warum ?](/kubernetes/pod-affinity-antiaffinity/warum.md)
     * [Übung](/kubernetes/pod-affinity-antiaffinity/uebung.md)

  1. Kubernetes - Kustomize 
     * [Beispiel ConfigMap - Generator](/kustomize/01-example-configmap.md)
     * [Beispiel Overlay und Patching](/kustomize/02-overlay-example.md)
     * [Resources](/kustomize/resources.md)

  1. Kubernetes Paketmanagement (Helm) 
     * [Warum ? (Dev/Ops)](/helm/warum.md)
     * [Grundlagen / Aufbau / Verwendung (Dev/Ops)](/helm/grundlagen.md)
     * [Helm - wichtige Befehle](/helm/befehle.md)
     * [Praktisches Beispiel bitnami/mysql (Dev/Ops)](/helm/example.md)

  1. Kubernetes - Storage 
     * [Praxis. Beispiel. NFS](/shared-volumes/nfs-multiple.md) 
  
  1. gitlab ci/cd
     * [Overview](/gitlab/01-ci-cd-overview.md)
     * [Using the test - template](/gitlab/02-example-testtemplate.md)
     * [Examples running stages](/gitlab/03-example-running-stages.md) 
     * [Predefined Vars](/gitlab/04-predefined-vars.md)
     * [Rules](/gitlab/05-rules.md)
     * [Example Defining and using artifacts](/gitlab/07-example-defining-and-using-artifacts.md)

  1. gitlab / Kubernetes (gitops) 
     * [gitlab Kubernetes Agent with gitops - mode](/gitlab/example-gitlab-kubernetes-agent-with-gitops-mode.md)  

  1. gitlab / Kubernetes (CI/CD - old-school mit kubectl) 
     * [Vorteile gitlab-agent](/kubernetes/gitlab/advantage-gitlab-agent.md)
     * [Step 1: Installation gitlab-agent for kubernetes](/kubernetes-gitlab-ci-cd/99-gitlab-agent-with-kubectl.md)
     * [Step 2: Debugging KUBE_CONTEXT - Community Edition](kubernetes-gitlab-ci-cd/04-fix-problem-context-auto-devops.md)
     * [Step 3: gitlab-ci.yml setup for deployment and sample manifest](/kubernetes-gitlab-ci-cd/05-setup-deployment-with-sample-manifest.md)

  1. gitlab / Kubernetes (CI/CD - Auto Devops) 
     * [Was ist Auto DevOps](/gitlab-ci-cd/was-ist-autodevops.md)
     * [Debugging KUBE_CONTEXT - Community Edition](kubernetes-gitlab-ci-cd/04-fix-problem-context-auto-devops.md)

  1. Prometheus 
     * [Prometheus/Grafana Überblick](/prometheus/overview.md)
     * [Prometheus Installation / Walkthrough](/prometheus/walkthrough-installation-setup.md)
  
  1. Tipps & Tricks 
     * [Default namespace von kubectl ändern](/kubectl/change-default-namespace.md)
     * [Ingress Controller auf DigitalOcean aufsetzen](/digitalocean/ingress-controller-aufsetzen-mit-helm.md)
     * [vi einrückungen für yaml](/vim/vim-yaml.md)
     * [gitlab runner as nonroot](/gitlab/gitlab-runner/non-root.md)
     * [curl zum Überprüfen mit Pod](/curlimages-curl.md)

  1. RootLess / Security 
     * [seccomp-profile-default docker](https://github.com/docker/docker-ce/blob/master/components/engine/profiles/seccomp/default.json)
     * [Pod Security Policy](/security/pod-security-policy.md)
     * [Pod Security Policy - Übung](/security/pod-security-policy-exercise.md)
     * [RunAsUser Exercise](/security/uebung-runasuser.md)
     * [Offizielles RootLess Docker Image für Nginx](https://github.com/nginxinc/docker-nginx-unprivileged) 

  1. Rechte 
     * [RBAC / Rechte allgemein](/rechte/general.md)

  1. Documentation
     * [helm dry-run vs. template](https://jhooq.com/helm-dry-run-install/)
     * [Marktuebersicht Kubernetes Hosting](/misc/kubernetes-hosting.md)

