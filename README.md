## 
kubectl -n fossa create secret docker-registry quay.io --docker-server=quay.io --docker-username=<username> --docker-password=<password> --docker-email=<email> --dry-run -o yaml >> docker-registry.yaml

add this docker-registry.yaml to template before running helm install command
