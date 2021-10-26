# helm-barney-buffet

This repository holds a collection Helm charts for deploymet on Kubernetes clusters

## Using this Helm Repository

This repository can be added to your Helm instance by running the `repo add` command.

```bash
helm repo add barney-buffet https://barneybuffet.github.io/helm-barney-buffet/
```

Once the repository is added to your helm instance, a chart can be installed with the `install` command.

```bash
helm install -n bitcoin tor barney-buffet/tor --create-namespace
```

## How to Host Your Own Helm repo

### Create a Helm chart

Initate/create a new helm chart with the `create` command.

```bash
helm create charts/tor
```

### Lint the Charts

To check your chart run the `lint` command on your chart.

```bash
helm lint charts/tor
```

### Create the Helm chart package

Once you are happy with the chart create the tgz package with the `package` command.

```bash
helm package charts/tor
```

### Add new chart

After you have packaged up your chart it can be added to the repository index with the `repo` command.

```bash
helm repo index --url https://barneybuffet.github.io/helm-barney-buffet/ --merge index.yaml .
```

#### References

* [How to host your Helm chart repository on GitHub](https://jamiemagee.co.uk/blog/how-to-host-your-helm-chart-repository-on-github/)
* [Create a public Helm chart repository with GitHub Pages](https://medium.com/@mattiaperi/create-a-public-helm-chart-repository-with-github-pages-49b180dbb417)
* [How to use github pages as your Helm Charts repository](https://blog.dahanne.net/2019/06/27/how-to-use-github-pages-as-your-helm-charts-repository/)