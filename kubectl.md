```bash
kubectl config get-contexts
kubectl config current-context
kubectl config use-context my-cluster-name

kubectl get namespace                                             # List namespaces on the current cluster
kubectl config set-context --current --namespace=ggckad-s2        # Enregistre de manière permanente le namespace pour toutes les commandes kubectl suivantes dans ce contexte

kubectl get [resource-type]              # resource-type like service, pod, deployment, ingress
kubectl get services                     # Liste tous les services d'un namespace
kubectl get pods --all-namespaces        # Liste tous les Pods de tous les namespaces
kubectl get pods -o wide                 # Liste tous les Pods du namespace courant, avec plus de détails
kubectl get pods -A -owide               # -A for --all-namespaces
kubectl get pods -owide --show-labels    # show labels
kubectl get pods -l=mytag=my-value       # filter pod on label
kubectl get pods --field-selector=status.phase=Running # filter by status

# Commandes Describe avec un affichage verbeux
kubectl describe pods my-pod
kubectl describe nodes my-node

kubectl exec -it [pod] -- /bin/sh # connect to the pod

kubectl logs my-pod                                 # Affiche les logs du pod (stdout)
kubectl logs my-pod -c my-container                 # Affiche les logs d'un conteneur particulier du pod (stdout, cas d'un pod multi-conteneurs)
kubectl logs -f my-pod                              # Fait défiler (stream) les logs du pod (stdout)

kubectl get no [node_name] -owide                   # Liste tous les Noeuds de tous les namespaces

kubectl scale deployment [deployment] --replicas=[number]  # Rescale deployment replicas

kubectl apply -f [resource].yaml # applying resource file
```
