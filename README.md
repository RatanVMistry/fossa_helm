## 
kubectl -n fossa create secret docker-registry quay.io --docker-server=quay.io --docker-username=<username> --docker-password=<password> --docker-email=<email> --dry-run -o yaml >> docker-registry.yaml

add this docker-registry.yaml to template before running helm install command

Install helm for fossa 
Run this command from fossa helm chart dire 
cd foss_helm/fossa

helm install --name fossa  --set fossahostname=<hostname for fossa>,hostip=<host ip for host>,miniohostname=<hostname for minio> --namespace fossa .


hostip is for single node k8s cluster. Provide vm publicIP as hostip.
Example:
miniohostname= minio.local
fossahostname= fossa.local
hostip = x.x.x.x
