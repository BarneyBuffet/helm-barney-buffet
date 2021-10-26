# TOR Helm Chart

This repository is a helm chart for `barneybuffet/tor`

* [Docker Hub barneybuffet/tor](https://hub.docker.com/r/barneybuffet/tor)
* [Github BarneyBuffet/docker-tor](https://github.com/BarneyBuffet/docker-tor)

## Using this helm chart

### Add helm repository

```bash
helm repo add barney-buffet https://github.com/BarneyBuffet/helm-barney-buffeti
```

## Dry Run

Try out the templating with a dry run

```bash
helm install -n admin --debug --dry-run tor ./charts/tor
```

```bash
helm install -n admin --debug --dry-run tor barney-buffet/tor
```

## Install chart

```bash
helm install -f .values.yaml -n admin tor ./charts/tor --create-namespace 
```

## Remove chart

```bash
helm uninstall -n admin tor
```


## Test tor is working

### Check inside the pod

```bash
curl --socks5 localhost:9050 --socks5-hostname localhost:9050 https://ipinfo.io/ip
curl --socks5 localhost:9050 --socks5-hostname localhost:9050 -s https://check.torproject.org/ | cat | grep -m 1 Congratulations | xargs
curl --socks5 127.0.0.1:9050 --socks5-hostname 127.0.0.1:9050 -s https://check.torproject.org/ | cat | grep -m 1 Congratulations | xargs
```

### Check outside the pod

```bash

curl --socks5 192.168.1.4:9050 --socks5-hostname 192.168.1.4:9050 https://ipinfo.io/ip
curl --socks5 192.168.1.4:9050 --socks5-hostname 192.168.1.4:9050 -s https://check.torproject.org/ | cat | grep -m 1 Congratulations | xargs
```

#### Reference

* [](https://github.com/MrChrisJ/fullnode/issues/6)