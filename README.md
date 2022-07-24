
# argocd-hard-refresher
A chart to enable hard-refresh to an umbrella chart applications in ArgoCD or target to another ArgoCD application. 

#### Usage:
The sub-chart Redis will be upgraded when 

    apiVersion: v2
    name: my-umbrella-chart
    description: A sample umbrella chart that need to be refreshed and noticed when Redis new version is published.
    type: application
    version: 1.0.0
    appVersion: 1.0.0
    
    dependencies:
      - name: redis
        version: "^16.2.1"
        repository: "https://charts.bitnami.com/bitnami"
      - name: argocd-hard-refresher
        version: "0.1.1"
        repository: "oci://ghcr.io/camposdelima"
