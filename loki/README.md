 helm upgrade --install loki grafana/loki-stack -f .\values.yaml --namespace monitoring --version 2.9.11

Release "loki" does not exist. Installing it now.
NAME: loki
LAST DEPLOYED: Thu Sep 14 10:26:48 2023
NAMESPACE: monitoring
STATUS: deployed
REVISION: 1
NOTES:
***********************************************************************
 Welcome to Grafana Loki
 Chart version: 5.20.0
 Loki version: 2.9.0
***********************************************************************

Installed components:
* grafana-agent-operator
* loki