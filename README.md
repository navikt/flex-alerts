# spoknad-alerts

Lager alerts for team sykmelding sine apper

For mer informasjon om hvordan alarmene fungere se: https://github.com/nais/doc/tree/master/content/alerts

## Utvikling

En kan bruke https://prometheus.nais.preprod.local/graph som hjelp til å teste queries.

## Deploy prod

All kode som er i master går til prod.

Det kan evt. gjøres manuelt med følgende kommandoer:
* For fss alerts: `kubectl apply --context prod-fss --namespace default -f spoknad-alerts.yaml`
* For sbs alerts: `kubectl apply --context prod-sbs --namespace default -f spoknad-alerts-sbs.yaml`

## For NAV ansatte
Vi er tilgjengelig på slack kanalen #spsøknad
