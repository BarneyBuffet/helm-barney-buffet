# helm-repository
My helm chart repository

## Install chart

```bash
clear && helm install -n downloaders sonarr ./charts/sonarr --create-namespace
```

## Remove chart

```bash
helm uninstall -n downloaders sonarr
```

## Dry Run

Try out the templating with a dry run

```bash
clear && helm install -n downloaders  --debug --dry-run sonarr ./charts/sonarr
```

## Reference

* [Docker Instructions](https://sonarr.tv/#downloads-v3-docker)
* [linuxserver/sonarr](https://docs.linuxserver.io/images/docker-sonarr)