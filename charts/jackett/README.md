# helm-repository
My helm chart repository

## Install chart

```bash
clear && helm install -n downloaders jackett ./charts/jackett --create-namespace
```

```bash
clear && helm upgrade -n downloaders jackett ./charts/jackett --create-namespace
```

## Remove chart

```bash
helm uninstall -n downloaders jackett
```

## Dry Run

Try out the templating with a dry run

```bash
clear && helm install -n downloaders  --debug --dry-run jackett ./charts/jackett
```