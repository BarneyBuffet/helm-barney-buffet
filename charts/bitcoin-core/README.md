
## Install chart

```bash
helm install -n bitcoin bitcoin-core ./charts/bitcoin-core --create-namespace
```

## Remove chart

```bash
helm uninstall -n bitcoin bitcoin-core
```

## Dry Run

Try out the templating with a dry run

```bash
helm install -n bitcoin  --debug --dry-run tor ./charts/bitcoin-core
```

#### References 

* [Running bitcoin node in a kubernetes cluster](https://medium.com/@Judezhu87/running-bitcoind-node-on-kubernetes-1d833212b1a)
* [](https://stadicus.github.io/RaspiBolt/raspibolt_30_bitcoin.html)