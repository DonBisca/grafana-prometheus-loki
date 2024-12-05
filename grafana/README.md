helm repo update grafana/grafana --version 6.60.1
helm upgrade --install grafana grafana/grafana -f .\values.yaml --namespace monitoring --version 6.60.1

waylet pro: 
helm upgrade --install grafana grafana/grafana -f .\values-grafana-wayletpro.yaml --namespace monitoring --version 6.60.1

kubernetes-pro:
helm upgrade --install grafana grafana/grafana -f .\values-grafana-kubernetes-pro.yaml --namespace monitoring --version 6.60.1




Release "grafana" does not exist. Installing it now.
NAME: grafana
LAST DEPLOYED: Thu Sep 14 10:09:55 2023
NAMESPACE: default
STATUS: deployed
REVISION: 1
NOTES:
1. Get your 'admin' user password by running:

   kubectl get secret --namespace default grafana -o jsonpath="{.data.admin-password}" | base64 --decode ; echo


2. The Grafana server can be accessed via port 80 on the following DNS name from within your cluster:

   grafana.default.svc.cluster.local

   Get the Grafana URL to visit by running these commands in the same shell:
     export POD_NAME=$(kubectl get pods --namespace default -l "app.kubernetes.io/name=grafana,app.kubernetes.io/instance=grafana" -o jsonpath="{.items[0].metadata.name}")       
     kubectl --namespace default port-forward $POD_NAME 3000

3. Login with the password from step 1 and the username: admin
#################################################################################
######   WARNING: Persistence is disabled!!! You will lose your data when   #####
######            the Grafana pod is terminated.                            #####
#################################################################################
