# argocd_dep

## argocd installation
- kubectl create namespace argocd
- kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
- kubectl get svc -n argocd
- kubectl port-forward -n argocd svc/argocd-server 8080:443  (to access argocd ui)
- login to ui-> user - admin, password - `kubectl get secret argocd-initial-admin-secret -n argocd -o yaml` , it wil be base64 encoded use `echo password | base64 --decode`

