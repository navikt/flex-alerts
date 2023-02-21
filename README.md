# flex-alerts

> tidligere kjent som spoknad-alerts

Lager alerts for team flex sine applikasjoner.

For mer informasjon om hvordan alarmene fungerer se: https://doc.nais.io/observability/alerts

## Alertmanager
Alerts status  https://alertmanager.prod-gcp.nav.cloud.nais.io/
Dev-gcp: https://alertmanager.dev-gcp.nav.cloud.nais.io/

## Metrics
En kan bruke https://prometheus.prod-gcp.nais.io/graph som hjelp til å teste queries.

## Deploy prod
All kode som er i master går til prod.

Det kan evt. gjøres manuelt med følgende kommandoer:
* For gcp alerts: `kubectl apply --context prod-gcp --namespace flex -f flex-alerts-gcp.yaml`
* For fss alerts: `kubectl apply --context prod-fss --namespace default -f flex-alerts.yaml`

## Sjekk at alerts kjører
* For gcp: `kubectl get alerts --context prod-gcp --namespace flex`
* For fss: `kubectl get alerts --context prod-fss`

## For NAV ansatte
Vi er tilgjengelig på Slack: `#flex`
