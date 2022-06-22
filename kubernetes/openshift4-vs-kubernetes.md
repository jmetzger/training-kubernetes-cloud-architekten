# OpenShift 4 vs. Kubernetes (Vergleich)

## Was ist OpenShift 4 in Bezug auf Kubernetes 

  * Die Entwickler von OpenShift 4 bezeichnen Kubernetes gerne als KERNEL, den Kern des Systems. 
  * Um diesen Kern gibt es entsprechende Erweiterungen, die sich an Kubernetes anlehnen 

## Detail: Welches Betriebssystem kann verwendet werden
  * Kubernetes: Jedes Linux OS
  * OpenShift: CoreOS

## Detail: Sicherheit für Pods (Container) 

  * Standardmäßig müssen in OpenShift Container als non-root laufen (+ für Openshift) 
  * OpenShift verwendet ein anderes Sicherheitskonzepten/Sicherheitsmodul als Kubernetes 
    * OpenShift: Security Context Contraints 
    * Kubernetes:  PodSecurityPolicies (PSP: alt), PodSecurityStandards (PSS: neu) 

## oc vs. kubectl 

  * oc ist eine Erweiterung von kubectl 
  * Es beherrscht die gleichen Kommandos und noch zusätzliche 

