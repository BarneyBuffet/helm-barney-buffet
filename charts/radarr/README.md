# helm-repository
My helm chart repository

## Install chart

```bash
clear && helm install -n downloaders radarr ./charts/radarr --create-namespace
```

## Remove chart

```bash
helm uninstall -n downloaders radarr
```

## Dry Run

Try out the templating with a dry run

```bash
clear && helm install -n downloaders  --debug --dry-run radarr ./charts/radarr
```

## Reference

* [Docker Instructions](https://radarr.tv/#downloads-v3-docker)
* [linuxserver/radarr](https://docs.linuxserver.io/images/docker-radarr)