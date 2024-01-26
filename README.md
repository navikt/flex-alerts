# flex-alerts

> tidligere kjent som spoknad-alerts

Lager alerts for team flex sine applikasjoner.

For mer informasjon om hvordan alarmene fungerer se: https://doc.nais.io/observability/alerts

## Alertmanager
Her finner man alle alerts og statusen dems nå: https://prometheus.prod-gcp.nav.cloud.nais.io/alerts?search=flex

Alerts som har fyrt av og sendt notifikasjon på slack finner man her https://alertmanager.prod-gcp.nav.cloud.nais.io/
her kan man også silence alerts

For å bestemme hvilke slack kanal alertene skal postes i så kan det endres her: https://console.nav.cloud.nais.io/team/flex/settings


## Metrics
En kan bruke https://grafana.nav.cloud.nais.io/explore som hjelp til å teste queries.

## Deploy prod
All kode som er i main går til prod og dev.

Det kan evt. gjøres manuelt med følgende kommandoer:
* For gcp alerts: `kubectl apply -f --context prod-gcp --namespace flex flex-alerts.yaml`

## Sjekk at alerts kjører
* For gcp: `kubectl get prometheusRule --context prod-gcp --namespace flex`

## For NAV ansatte
Vi er tilgjengelig på Slack: `#flex`
