# helm-repository
My helm chart repository

## Install chart

```bash
helm install -n downloaders transmission ./transmission --create-namespace \
  --set vpn.provider=<vpn> \
  --set vpn.username=<username> \
  --set vpn.password=<password> \
  --set transmission.username=<username> \
  --set transmission.password=<password>
```

## Remove chart

```bash
helm uninstall -n downloaders transmission
```

## Dry Run

Try out the templating with a dry run

```bash
clear && helm install -n downloaders  --debug --dry-run transmission ./charts/transmission
```