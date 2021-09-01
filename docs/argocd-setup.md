## Steps to use ArgoCD

### Vagrant
1. Start the virtual machine with `vagrant up`.
2. login to VM created by vagrant with `vagrant ssh`

### Install ArgoCD
1. If we follow the installation docs of argocd, we might end up with errors. ArgoCD team wants the users to give required permissions required for argocd. Use the following command to avoid errors `curl -sfL https://get.k3s.io | K3S_KUBECONFIG_MODE="644" sh -s -`.
2. copy [argocd-server-nodeport.yaml](https://github.com/udacity/nd064_course_1/blob/main/solutions/argocd/argocd-server-nodeport.yaml) and run it with `kubectl apply -f argocd-service.yaml`. Current password is `YA2hgP-1pyBXJwbS`.
3. login to argocd: username is admin and password can be extracted with `kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d`

### Some commands
1. get nodes: `kubectl get no`
2. get podes in all namespaces `kubectl get po -A`
3. get all podes in argocd namespace `kubectl get po -n argocd`
4. get all services in argocd namespace `kubectl get svc -n argocd`