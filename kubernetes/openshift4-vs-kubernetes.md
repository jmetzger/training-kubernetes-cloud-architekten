# OpenShift 4 vs. Kubernetes (Vergleich)

## Was ist OpenShift 4 in Bezug auf Kubernetes 

  * Die Entwickler von OpenShift 4 bezeichnen Kubernetes gerne als KERNEL, den Kern des Systems. 
  * Um diesen Kern gibt es entsprechende Erweiterungen, die sich an Kubernetes anlehnen 

## Detail: Welches Betriebssystem kann verwendet werden
  * Kubernetes: Jedes Linux OS
  * OpenShift 4: CoreOS

## Detail: Sicherheit für Pods (Container) 

  * Standardmäßig müssen in OpenShift Container als non-root laufen (+ für Openshift) 
  * OpenShift 4 verwendet ein anderes Sicherheitskonzepten/Sicherheitsmodul als Kubernetes 
    * OpenShift 4: Security Context Contraints 
    * Kubernetes:  PodSecurityPolicies (PSP: alt), PodSecurityStandards (PSS: neu) 

## Detail: Container bauen 
 
  * Kubernetes: Innerhalb von Kubernetes mit den nativen Tools von Kubernetes können keine Images gebaut werden
    * Das bauen von Images erfolgt ausserhalb von kubernetes z.B. mit docker, buildah 
  * OpenShift 4: Images können innerhalb von OpenShift 4 mit buildah gebaut werden. Es sind keine weiteren Tools notwendig 

## oc vs. kubectl 

  * oc ist eine Erweiterung von kubectl 
  * Es beherrscht die gleichen Kommandos und noch zusätzliche 

