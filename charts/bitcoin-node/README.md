



## Update Chart.yaml dependencies

```bash
helm dep update
```

## Install with private values

```bash
helm install -f .values.yaml -n test bitcoin-node .
```