# flex-alerts

> tidligere kjent som spoknad-alerts

Lager alerts for team flex sine applikasjoner.

For mer informasjon om hvordan alarmene fungerer se: https://doc.nais.io/observability/alerts

## Alertmanager
Her finner man alle alerts og statusen dems nå: https://prometheus.prod-gcp.nav.cloud.nais.io/alerts?search=flex

Alerts som har fyrt av og sendt notifikasjon på slack finner man her (tror jeg) https://alertmanager.prod-gcp.nav.cloud.nais.io/

For å bestemme hvilke slack kanal alertene skal postes i så kan det endres her: https://console.nav.cloud.nais.io/teams/flex


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
