<p align="center">
  <img src="etzba.png" alt="etzba"/>
</p>

# charts

In this repository you'll find etzba helm charts, to deploy in your kubernetes cluster. To read more about etzba tools, go to https://etzba.com.

For every chart there is a dedicated section with the relevant command to install the chart.

### image-updater

Add:

```sh
helm repo add image-updater https://raw.githubusercontent.com/etzba/charts/master/image-updater
helm repo update
helm repo list
```

Install:

```sh
helm install image-updater image-updater/ -n image-updater --create-namespace
```

### secret-distributor

Add:

```sh
helm repo add secret-distributor https://raw.githubusercontent.com/etzba/charts/master/secret-distributor
helm repo update
helm repo list
```

Install:

```sh
helm install secret-distributor secret-distributor/ -n secret-distributor --create-namespace
```